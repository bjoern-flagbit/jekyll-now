---
layout: post
title: chmod Spickzettel
description: Kleine Übersicht zum chmod Befehl in Linux
---
#### Beispiel Ausgabe vom Befehl "ls -l" im Terminal zu einer example.txt Datei

	-rw-r--r--  1  www-data  1000  1892  Jul 17  18:01 example.txt

In dem oben gezeigtem Beispiel gehört die Datei dem User *www-data* und der Gruppe *1000* an.

#### Beispiel Befehl um die Berechtigungen der Datei zu ändern (Oktal-Modus)

	chmod 644 example.txt

**Wichtig:** In Linux gibt es 3 verschiedene Typen von Berechtigungen pro Datei/Ordner! 

* 4 / read / lesen (r)
* 2 / write / schreiben (w)
* 1 / execute / ausführen (x)

__*Übersetzt bedeutet unser chmod-Befehl von oben also:*__  
Der Eigentümer darf lesen und schreiben, weil 4 + 2 = 6 (1. Stelle ist der Eigentümer).  
Die Gruppe darf nur lesen, weil 4 = 4  (2. Stelle ist die Gruppe).  
Jeder andere darf ebenfalls lesen, weil 4 = 4 (3. Stelle ist jeder andere).

#### Praktische Beispiele

**chmod 400** *example.txt* **read by owner**  
**chmod 040** *example.txt* **read by group**  
**chmod 004** *example.txt* **read by anybody (other)**  

**chmod 200** *example.txt* **write by owner**  
**chmod 020** *example.txt* **write by group**  
**chmod 002** *example.txt* **write by anybody (other)**  

**chmod 100** *example.txt* **execute by owner**  
**chmod 010** *example.txt* **execute by group**  
**chmod 001** *example.txt* **execute by anybody (other)**  

#### Nummern für chmod Berechtigungen

**7** = |  &nbsp;4 + 2 + 1&nbsp; |  read/write/execute bzw. lesen/schreiben/ausführen  
**6** = |  &nbsp;4 + 2&nbsp; |  read/write bzw. lesen/schreiben  
**5** = |  &nbsp;4 + 1&nbsp; |  read/execute bzw. lesen/ausführen  
**4** = |  &nbsp;4&nbsp; |  read bzw. lesen  
**3** = |  &nbsp;2 + 1&nbsp; |  write/execute bzw. schreiben/ausführen    
**2** = |  &nbsp;2&nbsp; |  write bzw. schreiben  
**1** = |  &nbsp;1&nbsp; |  execute bzw. ausführen  

Das war's auch schon mit dem Spickzettel.

Weitere Ressourcen:
[Wiki Chmod Ubuntuusers.de](https://wiki.ubuntuusers.de/chmod/)