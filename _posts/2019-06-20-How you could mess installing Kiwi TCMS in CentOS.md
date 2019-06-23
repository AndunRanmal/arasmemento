---
layout: post
title:  "How You Could Not Mess Installing Kiwi TCMS in CentOS"
author: andun
categories: [ Technology ]
featured: false
image: assets/images/kiwi.jpg
---

##### What is so important of Kiwi
As simply Kiwi is a Test Plan, Test Run and a Test Case Management system. The most grateful thing in Kiwi is, it’s an open source tool written in Python and Django. So anyone can get a pull of the project and set it up on your own server or on docker environment and you can add missing features by forking the git project and contribute. Also it has an active community. So if you stuck in installation process or on feature wise you could contact them with the support mail and they will get back to you in no time.  
Kiwi TCMS features Bugzilla, GitHub, GitLab and JIRA integration, fast test plan and runs search, powerful access control for each plan, run and case, and XML-RPC APIs.
XML-RPC API is the api client that Kiwi has exposed to the outside world. With it, the user has been enabled to create different plugins for users’ requirement. 
There are 2 methods that you can deploy Kiwi. 
In a docker container
Or on a virtual machine 

In this article, I’ve discussed how to install Kiwi in a CentOS VM with postgreSQL. And what possible difficulties you will be facing during this deployment. 


##### Installing Kiwi on CentOS

###### 1. Prerequisites:

  * Python 3.5 or 3.6 (Currently installed with python 3.5)
  * Postgres server 9.4 or higher  (Installed in Postgres 10.0 )


###### 2. Install Python 3.5 in Centos

Use the instructions in the following link to install python3.5 via software collection org

https://www.softwarecollections.org/en/scls/rhscl/rh-python35/

###### 3. Get source code

  `git clone https://github.com/kiwitcms/Kiwi.git`

###### 4. Setup virtual env

If you have installed python according to step 2. You should enable python3.5 on bash with
scl enable rh-python35 /bin/bash

  * Then to create virtual env run the following command

    `virtualenv ~/virtualenvs/kiwi`

  * Install dependencies on Centos

      Install following dependencies needed to compile some python dependencies

      `sudo yum install gcc python-devel MariaDB-devel libxml2-devel     libxslt-devel graphviz`

      Install following dependencies for the development after navigating to created virtual env and to the cloned project with following commands respectively.

      `. ~/virtualenvs/kiwi/bin/activate`
      `pip install -r requirements/postgres.txt`
      `pip install -r requirements/devel.txt`
      `pip install python2-secret`
      `cd tcms/`
      `npm install`
      
###### Possible issues
  * Dependency download failed as Pip tool is not upgraded.
          `Pip install -U pip`
  * Dependency installation failed as setuptools are not upgraded
          `Pip install -U setuptools`

###### 5. Initialize Database

Development environment Kiwi defaultly configured to use SQLite as the database. As we use postgres it should be configured in <project_dir>/tcms/settings/devel.py as the following.
```
DATABASES = {
	'default': {
   	'ENGINE': 'django.db.backends.postgresql_psycopg2',
   	'NAME':'<db_name>',
   	'USER': '<db_user>',  //postgres user for the account
   	'PASSWORD': '',
   	'HOST': 'localhost',
   	'PORT': '',
	}
}
```

And run the following command to create the database schema

`./manage.py migrate`


###### Possible issues:

  * Error with following exception
  
  ```
    raise ImproperlyConfigured("Error loading psycopg2 module: %s" % e)
    django.core.exceptions.ImproperlyConfigured: Error loading psycopg2 module: No module named 'psycopg2'`
    Solution:
    pip uninstall psycopg2
    pip uninstall psycopg2-binary
    pip install psycopg2-binary
    Error with following Programming error
    django.db.utils.ProgrammingError: syntax error at or near "WITH
    ORDINALITY"
    LINE 6:                     FROM unnest(c.conkey) WITH ORDINALITY co...
  ```

This is because installed postgres server version is not compatible with installed django. You have to use postgres 9.4 or higher version



###### 6. Create a super user for Kiwi with following command

`./manage.py createsuperuser`

###### 7. Run server

`./manage.py runserver`

And Kiwi python server starts on http://127.0.0.1:8000/  

###### 8. Configure Apache for a proxy pass

To access Kiwi server we need to add a proxy pass for the url in apache virtual host




