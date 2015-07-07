=======
Notizen
=======

Allgemeines zur Dokumentation
-----------------------------

Für das Projekt müssen mindestens die folgenden Dokumentationen vorliegen.

	- Introduction (Einführung)
		- Problem Beschreibung
		- Ziele (Goals)
		- Nicht Ziele (Non Goals)

	- Changelog

Die Dokumentationen sollten im **rst-Format** geschrieben werden. 


Meilensteine
""""""""""""
Bennenung der Meilensteine
	- name: Projektname - Kurze genaue Beschreibung



Standard nexiles setup für python
---------------------------------

In jedem Projekt sollte ein *src* und ein *docs* Ordner vorhanden sein. 
Im docs Ordner werden alle Dokumentationen gespeichert und im src Ordner die ganzen Code-Dateien.
Um ein standard setup zu erstellen, wird im *src* Ordner ein weiterer Order mit dem Projektname erstellt. Hier liegt die setup.py Datei und ein weiterer angelegter Ordner mit dem ersten Teil des Projektnamens. Hier wird noch ein weiterer Ordner angelegte mit dem zweiten Teil des Projektnamens. Übersichtshalber sieht das wie folgt aus:

