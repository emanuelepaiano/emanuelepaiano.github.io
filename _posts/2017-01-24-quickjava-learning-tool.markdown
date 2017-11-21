---
layout:     post
title:      "Quickjava, a simple learning tool for novices"
subtitle:   "Learning Java in a procedural style"
date:       2017-01-24 12:00:00
author:     "Emanuele Paiano"
header-img: "img/home-bg.jpg"
---

<p>By QuickJava, you can write Java program in a procedural paradigm, without classes concepts (useful for newbie).</p>

<p><a href="https://github.com/emanuelepaiano/quickjava">Github repository</a></p>

<p>If you run it on a Linux host, you need Oracle JDK or Openjdk, bash terminal, MAKE tools and a text editor (nano or gedit) installed on your linux distro. If you want run qjide (GUI version), you need QT libs 4.8.</p>

<p>QuickJava can be runned on Windows using Cygwin environment and Notepad++ as editor.</p>

<a href="#">
    <img src="https://github.com/emanuelepaiano/quickjava/blob/master/screenshot.png?raw=true" alt="Screenshot">
</a>

<h2 class="section-heading">WRITING THE FIRST PROGRAM: HELLO WORLD</h2>
<p>Open terminal, move into quickjava directory and create new project with make:</p>
<pre>
     user@hostname ~/quickjava $ make new PRJ=my_project
     Creating main.java..OK
     Generating Makefile..OK
     Makefile found
     Project my_project created into directory workspace 
     Copying libs to workspace/my_project/lib/ ...OK
</pre>

<p>You can see your project into workspace/ folder. You should write code into main() function
     into workspace/my_project/main.java file. For output stream, you can use standard Java statement, like
     System.out.print() or System.out.println().</p>
    
 <p>Example:</p>
    
<pre>
     void main(String[] args)
     {
      System.out.print("Hello Word!\n");
     }
 </pre>
     
     
<p> To run it, type 'make run PRJ=my_project' in terminal:</p>

<pre>
     lele@ema-notebook ~/quickjava $ make run PRJ=my_project
     Removing old class files..OK
     Removing old java files..OK
     Creating Java code from quickjava sources..OK
     Creating class files..OK
     Creating jar files..OK
     Removing old class files..OK
     Running..

     Hello Word!
     QuickJava program terminated successfully.
 </pre>
  
  
  <p> The compiled jar file is into workspace/my_project/build/Main.jar. 
  The "translated" java file is into jsrc/ directory.</p>


<h2 class="section-heading">Install</h2>

<p>For install tutorials, writing new class and libs, you can read <a href="https://github.com/emanuelepaiano/quickjava/blob/master/doc/START.TXT">docs/start.txt file</a></p>


