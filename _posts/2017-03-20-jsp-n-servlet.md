---
layout: post
title:  "JSP සහ Servlets"
author: andun
categories: [ Technology ]
image: assets/images/jspnservlet.jpg

---

මොනවාද මේ jsp සහ servlets කියන්නේ කියල අපි ඉස්සෙලම බලමු. JavaServer Pages(JSP ), servlets  කියන්නේ java language එක භාවිතා කරන තවත් technology එකක්. මෙම තාක්ෂනය භාවිතා කරන්නේ බොහෝ විට dynamic web  pages සැකසීම සදහා.  Java language එකට අමතරව මෙය HTML, XML  මත පදනම් වෙමින් ගොඩනැගේ .

JSP page එකක code එකක් සාමන්‍ය HTML page එකක code එකකට වඩා වෙනස් වෙන්නේ එහි තියෙන java ee language එකෙන් ලියපු code ඇතුලත් නිසා. මේ java ee code වලින් තමයි අපි server side  එකේ වෙන functions ටික ලියන්නේ. හරියට HTML code එක ඇතුලේ තියෙන php code එක වගේ. php වල code එක ලියන්නේ <?php …….. ?>  enclose එක ඇතුලේ වගේ, JSP වල ලියද්දි අපි භාවිතා කරන්නේ  <% ….. %> යන enclose එක. Browser එකට jsp වලින් request එකක් දුන්නම වෙන දේ බලන්න කලින් java servlet ගැනත් තව පොඩි idea එකක් අරන් ඉන්න එක හොඳි කියල හිතෙනවා.

Java servlet එකක් run කරන්න අපිට server එකක් ඕනේ වෙනවා. අපි බොහෝවිට බාවිතා කරන්නේමේ සදහා Apache Tom Cat server එකයි. මෙවැනි servlet එකක් run කිරීමෙන් අපිට ලැබෙන output එක තමයි සාමාන්‍ය HTML page එකක්. මෙ සදහා අවශ්‍ය වන java code ටික තමයි මේ servlet එකේ තියෙන්නේ. මිට අමතරව දැනගන්න ඕනේ තවත් දෙයක් තමයි servlet එකක HTML code  තියෙන්නේ java  code එක ඇතුලෙ කියන එක.

දැන් අපි බලමු browser එකට request එකක් අවම මොකද්ද වෙන්නේ කියල. සාමාන්‍ය .html .php වලින් browser එකට request එකකට වඩා වෙනස්. එකට හේතුව තමයි පළමුව jsp file එකේ තියෙන java code එක compile කිරීමේ අවශ්‍යතාවය. මේ සදහා idea එකක් ගන්න පහල රුපය අද්‍යනය කරමු. 

![walking]({{ site.baseurl }}/assets/images/jsp.png)

ඉහත රුපයට අනුව browser මගින් get request  එකෙන් hello.jsp file එක call  කරාම jsp container එක වන tom cat server එක jsp file එකේ තියෙන code එක කියවා, සම්පුරන්යෙන්ම java  code  එකක් බවට හරවනවා. මෙම java  code එක පසුව server  එකෙන් compile කරන කොට java class එකක් හදාගන්නවා. මෙම java class එක තමයි අපිට browser එකෙන් HTML page එකක් විදියට responseකට ලැබෙන්නේ.

දැන් ඔබ දන්නවා JSP සහ servlet  අතර වෙනස සහ එවයි ප්‍රදාන අරමුණ මොකක්ද කියන එක. ඒවගේම jsp file එකෙන් කොහොමද web  page එකක් execute කරන්නේ කියන එක. ඉදිරි articles වලින් බලමු කොහොමද servlet එකක් ලියගෙන්නේ සහ කොහොමද simple webpage එකක් jsp බාවිතයෙන් හදාගන්නේ කියල.
