---
layout:     post
title:      "SerialDuino, Yet another Java Arduino Serial Monitor"
subtitle:   "Connecting Java threads with Arduino"
date:       2017-10-05 23:49:00
author:     "Emanuele Paiano"
header-img: "img/asimov.jpg"
---

<h2 class="section-heading">About this project</h2>
Using this tool you can communicate with Arduino (compatible devices) using a special Java class directly within a thread.
Serialduino support following connection types:
<ul>
<li>COM ports</li>
<li>TCP/IP</li>
<li>Bluetooth RFCOMM</li>
</ul>

## How does it work?
Connection is based on a serial monitor class (ArduinoSerialMonitor.java). This class call some LinkDevice methods to communicate with Arduino. 
LinkDevice is an interface implemented from devices class, like ComLinkDevice, BluetoothLinkDevice and TcpLinkDevice.

<img src="https://github.com/emanuelepaiano/serialduino/blob/master/img/image.jpg">

<br>

##Demo

If you want to connect to Arduino using COM port, you need pass ComLinkDevice to ArduinoSerial Monitor object:

<pre>
     if (ComLinkDevice.isPortAvailable()){
			
	// COM Port for Linux
	//ComLinkDevice port=new ComLinkDevice(ComLinkDevice.getPortByName("ttyUSB0"), ComLinkDevice.BAUDRATE_9600);
			
	// COM Port for Windows/Dos
	//ComLinkDevice port=new ComLinkDevice(ComLinkDevice.getPortByName("COM1"), ComLinkDevice.BAUDRATE_9600);
			
			
	// First COM serial port
	ComLinkDevice port=new ComLinkDevice(ComLinkDevice.getPorts()[0], ComLinkDevice.BAUDRATE_9600);
			
	ArduinoSerialMonitor arduinoSerial=new ArduinoSerialMonitor(port);
			
	/* ........ */
			
 }
</pre>

you can find port automatically using getPorts() (it returns an array ports), or calling <i>getPortByName()</i>, passing port's name (name can changes on different operating systems). 
<br>Next step is open connection and communicate with Arduino, using <i>open()</i>, <i>send()</i> and <i>receiveString()</i> method:
<pre>
            //open and wait for arduino reboot
			arduinoSerial.open();
			
			//if device ready, send "hello" string to Arduino
			arduinoSerial.send("hello");
			
			//Receive echo response: you should see "hello" on java console
			System.out.print(arduinoSerial.receiveString());
</pre>

you can close connection with <i>close()</i> method:

<pre>
            //Close connection
			arduinoSerial.close();
</pre>

<br>

See src/org/serialduino/examples for bluetooth and tcp examples.

## Dependencies: 
SerialDuino require jSSC, for com support driver - https://code.google.com/archive/p/java-simple-serial-connector/

## Install
Import this code into your Eclipse project. You need include jssc.jar and jssc-2.7.0-javadoc.jar for serial support. 

### License
Apache 2.0 - http://www.apache.org/licenses/LICENSE-2.0

### Author
Emanuele Paiano - nixw0rm [at] gmail [dot] com
