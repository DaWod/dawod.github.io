---
layout: post
title:  "Javac und die Packages"
---

Java Beispiele aus einem Buch zum Laufen bringen...

```
packages javagames.util;
```
Eine solche Anweisung bedeutet, dass die Quelldateien im Verzeichnis javagames\util liegen müssen (Windows-Guy ;-)):
Zusätzlich gibt es noch ein Render-Verzeichnis, dort liegt ebenfalls ein Java-Source-File.

Die Kompilierung erfolgt durch
```
javac -d classes -sourcepath src src\javagames\util\FrameRate.java src\javagames\render\HelloWorldApp.java
```

Der Aufruf der kompilierten Dateien erfolgt dann durch
```
java -classpath classes javagames.render.HelloWorldApp
```
