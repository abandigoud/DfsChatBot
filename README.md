# DfsChatBot

DfsChatBot is a chat bot for  that's written in Java.  It is named after the first name given to the Java programming language before it became "Java".
 
DfsChatBot is most active in the [Java](https://chat.stackoverflow.com/rooms/139) and [Java and Android era](https://chat.stackoverflow.com/rooms/19132) chat rooms.

# Requirements

* Java 1.8
* [Maven](http://maven.apache.org) (for building)

# Build Instructions

To build the project, run the command below.

`mvn package`

This command will build the project and package it into an executable, shaded JAR. A shaded JAR file contains all of the project's dependencies. The shaded JAR file is saved here: `target/DfsChatBot-VERSION.jar`.

# Deploy Instructions

1. Copy the following files to the server. Put them in the same directory:
   1. `target/DfsChatBot-VERSION.jar`: The executable, shaded JAR file that contains DfsChatBot's code and dependencies.
   1. `bot.properties`: This file contains configuration data, such as the bot's login credentials. A sample file is located in the root of this project.
   1. `logging.properties` (optional): The configuration file for the Java Logging API.  A sample file is located in the root of this project.
1. Run DfsChatBot: `java -jar DfsChatBot-VERSION.jar &`  
   1. The "&" at the end of the command launches the program in the background.  This is useful if you are logged into a server remotely and need to logout after launching DfsChatBot.

# db.json

This is the file DfsChatBot uses to persist information, such as how many commands it has responded to and what rooms it has joined. It is located in the bot's working directory. The file will automatically be created if it doesn't exist.

# bot.properties

Contains various configuration settings for the bot. Open the sample "bot.properties" file at the root of this project for a description of each setting.

DfsChatBot must be restarted if any of these settings are changed while DfsChatBot is running.

# Adding/Removing Commands

To add a command, create an instance of the [Command]
