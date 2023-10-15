# phrasebook
Clojure for the Brave and True, JVM exercise, chapter 12

## Commands

### Compile & Run PiratePhrases
-- inside phrasebook
javac PiratePhrases.java
java PiratePhrases

### Play with -classpath
-- inside phrasebook
java -classpath /tmp PiratePhrases -- expect error
java -classpath /tmp:. PiratePhrases --it works because of directory . for Windows use ; for Mac/Linux use :

### Play with -classpath and packages
-- inside phrasebook/pirate_phrases
javac ../PirateConversation.java -- expect error, because javac is trying to find the directory phrasebook/pirate_phrases/pirate_phrases, and it happens because the classpath is current directory .
javac -classpath ../ ../PirateConversation.java -- now it works, because the classpath is the parent directory ../

### Jar Files
-- create the JAR with `jar cvfe [jar-name] [entry-point-class] [classes-to-add-into-jar...]`
jar cvfe conversation.jar PirateConversation PirateConversation.class pirate_phrases/*.class

-- run jar
java -jar conversation.jar
