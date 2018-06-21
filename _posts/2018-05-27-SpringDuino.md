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
<li>Robotic interface by Spring</li>
</ul>

Download available on <a href="https://github.com/emanuelepaiano/serialduino">Github repository</a>

<h2 class="section-heading">How does it work?</h2>
Connection is based on a serial monitor classes (SerialDuino). This class call some LinkDevice methods to communicate with Arduino by serial port (or wifi). 


<img src="https://github.com/emanuelepaiano/serialduino/blob/master/img/image.jpg?raw=true">
 

<h2 class="section-heading">License</h2>
<a href="http://www.apache.org/licenses/LICENSE-2.0">Apache 2.0</a>
