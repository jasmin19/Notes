=======
Notizen
=======

Datenbanken
===========

Primär- und Fremdschlüssel
^^^^^^^^^^^^^^^^^^^^^^^^^^

Primärschlüssel 
"""""""""""""""

Bei den Adressen haben wir die *ID* – diese ist der Primärschlüssel der Tabelle **Adressen**. In dieser Spalte enthaltene Werte dürfen nur ein einziges Mal vorkommen. Duplikate sind niemals erlaubt! Ein anderer Primärschlüssel ist in der Tabelle **PLZ** die Spalte *plz* und in der Tabelle **Anrede** die Spalte *kuerzel*.

Fremdschlüssel
"""""""""""""""

Was bei der Verknüpfung in der einen Tabelle der Primärschlüssel ist, ist in der zweiten Tabelle der Fremdschlüssel. Der Fremdschlüssel enthält den gleichen Wert wie der Primärschlüssel, kann aber öfters vorkommen (je nach Beziehungsart). So kann er einmal, keinmal oder mehrmals vorkommen.

In unserem Beispiel ist bei der Tabelle **PLZ** das Feld *plz* der Primärschlüssel und in der Tabelle **Adressen** das Feld *PLZ* der Fremdschlüssel (kann öfters vorkommen).

Bei der Tabelle **Anrede** ist das *akuerzel* der Primärschlüssel und in der Tabelle **Adresse** die Spalte *akuerzel* der Fremdschlüssel.

Tabelle: Adresse:

	==== ======== ========= ========
	id 	 name	  akuerzel	plz 
	==== ======== ========= ========
	1	 Susi	  w 		72074	
	2	 Peter 	  m 		72070
	==== ======== ========= ========


Tabelle: Plz:

	========== ==========
	PLZ 		ort	
	========== ==========
	72070		Tübingen
	72074		Tübingen
	========== ==========


Tabelle: Anrede:

	========== ==========
	akuerzel	Anrede 
	========== ==========
	w 			Frau
	m 			Herr
	========== ==========