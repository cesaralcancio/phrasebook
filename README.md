# phrasebook
Clojure for the Brave and True, JVM exercise

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



