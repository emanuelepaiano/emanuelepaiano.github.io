---
layout:     post
title:      "Quickjava, a simple learning tool for novice"
subtitle:   "Learning Java in a procedural style"
date:       2017-01-24 12:00:00
author:     "Emanuele Paiano"
header-img: "img/home-bg.jpg"
---

<p>QuickJava has been shared on github, so you can download and start to coding.</p>

<p>To run on a Linux host, you need Oracle JDK or Openjdk, bash terminal, make tools and a text editor (like nano or gedit) installed on your linux distro.</p>

<p>You can run QuickJava on Windows by Cygwin environment and notepad++ editor.</p>

<h2 class="section-heading">WRITING THE FIRST PROGRAM: HELLO WORLD</h2>
<p>Open terminal, go into quickjava directory and create new project into workspace:</p>
<pre>
     user@hostname ~/quickjava $ make new PRJ=my_project
     Creating main.java..OK
     Generating Makefile..OK
     Makefile found
     Project my_project created into directory workspace 
     Copying libs to workspace/my_project/lib/ ...OK
</pre>
<p>
     Now you can find your project into folder workspace/. We must edit main() function
     into workspace/my_project/main.java file. To write on screen use default java statement
     System.out.print() or System.out.println().</p>
    
    <p>This is final code into main.java:</p>
    
<pre>
     void main(String[] args)
     {
      System.out.print("Hello Word!\n");
     }
     </pre>
<p> We can run with 'make run PRJ=my_project' in terminal:</p>
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
    <p> The compiled jar file is present into build/Main.jar inside 
     my_project directory in workspace. The "translated" java file 
	 is present into jsrc/ directory.</p>




<h2 class="section-heading">Reaching for the Stars</h2>

<p>As we got further and further away, it [the Earth] diminished in size. Finally it shrank to the size of a marble, the most beautiful you can imagine. That beautiful, warm, living object looked so fragile, so delicate, that if you touched it with a finger it would crumble and fall apart. Seeing this has to change a man.</p>

<a href="#">
    <img src="{{ site.baseurl }}/img/post-sample-image.jpg" alt="Post Sample Image">
</a>
<span class="caption text-muted">To go places and do things that have never been done before – that’s what living is all about.</span>

<p>Space, the final frontier. These are the voyages of the Starship Enterprise. Its five-year mission: to explore strange new worlds, to seek out new life and new civilizations, to boldly go where no man has gone before.</p>

<p>As I stand out here in the wonders of the unknown at Hadley, I sort of realize there’s a fundamental truth to our nature, Man must explore, and this is exploration at its greatest.</p>

<p>Placeholder text by <a href="http://spaceipsum.com/">Space Ipsum</a>. Photographs by <a href="https://www.flickr.com/photos/nasacommons/">NASA on The Commons</a>.</p>
