---
layout:     post
title:      "SpringDuino, an Arduino MVC service for Spring"
subtitle:   "Interfacing Spring framework with Arduino"
date:       2018-05-27 18:49:00
author:     "Emanuele Paiano"
header-img: "img/arduino2.jpg"
---

<h1 class="section-heading">About this project</h1>
Using this tool you can interface Arduino (or enterprise boards) with Spring framework and REST services.
This project can be used for:
<ul>
<li>Building small domotics and IoT control panel</li>
<li>Interfacing roboting application with Java Spring</li>
</ul>

Download available on <a href="https://github.com/emanuelepaiano/SpringDuino">Github repository</a>

<h2 class="section-heading">How does it work?</h2>
Connection is based on a Java arduino serial monitor (<a href="https://github.com/emanuelepaiano/serialduino">SerialDuino</a>).


<h1 class="section-heading">Web access credentials:</h1>
<ul>
<li>User: root - pass: password</li>
<li>User: admin - pass: password</li>
<li>User: guest - pass: password</li>
</ul>

You can change login settings into src/main/webapp/WEB-INF/context-security.xml
 

<h2 class="section-heading">License</h2>
<a href="http://www.apache.org/licenses/LICENSE-2.0">Apache 2.0</a>
