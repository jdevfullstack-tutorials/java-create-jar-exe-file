# Java Create JAR Exe Tutorial
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fxdvrx1%2Fjava-create-jar-exe-file-tutorial&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=PAGE+VIEWS&edge_flat=false)](https://hits.seeyoufarm.com)

## Setting The Windows System Environment
1. Without the compiler added to the `Path`, you cannot use
   Java in the Command Prompt.

2. First, install the latest Java SE from:
	
   <https://www.oracle.com/technetwork/java/javase/downloads/index.html>

3. After that, in your computer, go to `System Properties`, you select
   `Advanced System Settings`. Or, you can directly search:
	
	```	
	Environment Variables
	```
   
   but, it is better to go to `System Properties` in 
   `Control Panel`, because sometimes,
   coming from search, the computer will not allow you to
   edit the System Variables. 

4. You should now be at Environment Variables window.
   At the bottom, you will see
   System Variables, select `Path`, then click `Edit`.

5. You should add there the directory of the Java compiler.
   Copy and paste that at the last part, but be careful!
   It contains several information that should not be deleted.
   
   And, when you don't see the last semicolon `;`
   from the last directory, you should add that.
   Mine is:
	
	```
	;C:\Program Files (x86)\Java\jdk1.8.0_144\bin;
	```

6. To check whether this is successful, open
   the Command Prompt and type
	
	```
	javac
	```

   then hit `Enter`,
   if the Command Prompt gives you information,
   then it is successfully added.

## Compiling & Running The Java Source Code Through The Command Prompt
1. Change the directory to where you put your source code.

2. But it is better you put your code on the Desktop directory.

3. If the code is on the Desktop, then open CMD, then type
         
	```
	cd Desktop
	```
   
   then hit `Enter`, this will bring you to the Desktop.
   
4. First, you need to compile the Java code in order to run the code.
5. Type `javac` followed by the filename with the filename extension.
   Example:
	
	```
	javac MyFirstProgram.java
	```
   
   then hit `Enter`.

6. If this is correct, then it will bring you to the next line.

7. Then, type 
	
	```
	java MyFirstProgram
	```

   then hit `Enter`, this will run your code.

8. Now, you have the class file and the java file. It is ready
   for creating the Executable JAr File.

## Creating The Executable JAR File
Remember that Java is a high-level 
 programming language
 and the creators of this language put some 
 barrier on direct manipulation
 of the memory for security reasons,
 unlike C that has a direct access to memory.

Also, one implication is that 
 Java should be portable
 to any OS. Hence, there is the Java Runtime Environment
 that contains the Java Virtual Machine 
 to fulfill such a thing.       

With that, creating the standard executable file is somewhat different. 
 Hence, they call it as Executable JAr File.
 JAr stands for Java Archive. 

1. Given you are done with the compilation,
    you need to create the  manifest file.
    Within the same directory
    create a text document (.txt), 
    name it as `manifest.txt`
    so that calling the file will not be hard.
    Open that and type
    	
	```
	Main-Class: MyFirstProgram
	```
         
    hit `Enter` twice then save the changes.

   You need to hit `Enter` twice.
    Java will fulfill
    a metadata within the manifest file too.

    Here, I am just using the above example. Of course,
     if the name of the class file is different,
     then that should be the name instead of `MyFirstProgram`.
         
2. Then after that you are now ready to create the 
     Executable JAr File.
 
    Open the Command Prompt and change the directory again
     to where you put your code.
    Then type
    
	```
	jar cfm MyFirstProgram.jar manifest.txt MyFirstProgram.class
	```   
	
    then hit `Enter`.

   If you have multiple class files, then include them too. 
    Again, I'm using the above example for continuity.
    To test whether this is successful, double click the new
    Executable JAr File, and if the program runs, you're done!
    Happy coding!

***
## Useful Links
<https://introcs.cs.princeton.edu/java/85application/jar/jar.html>

<https://www.javatpoint.com/how-to-make-an-executable-jar-file-in-java>

