=======
Notizen
=======

Models
======

Die Basisklasse für alle Modelle heißt **db.Model**.

Um eine Spalte zu definieren benutzt man **Column**. Der Name der Spalte ist der Name, den man zugewiesen hat. Wenn man jedoch einen anderen Name in der Tabelle nutzen möchte, kann man das als optionales erstes Argument festelgen.
Primärschlüssel sind gekennzeichnet durch folgendes::
	
	primary_key=True 


Die Spaltentypen sind das erste Argument von **Column**.
Die folgenden Typen sind die häufigsten:

===============  ======================================================
Typen			 Beschreibung
===============  ======================================================
*Integer*	     eine ganze Zahl
*Sting(size)*	 eine Zeichenkette mit maximaler länge
*Text*			 längerer Unicode-Text
*DateTime*		 Datum und Zeit, ausgedrückt in Python Datetime-Objekt
*Float*			 speichert Gleitkommazahlen
*Boolean*		 speichert boolesche Werte
*PickleType*	 speichert ein eingelegtes Python-Objekt
*LargeBinary*	 speichert große willkürlche Binärdaten
===============  ======================================================

Ein kleines Code-Beispiel::

	class User(db.Model):
	    id = db.Column(db.Integer, primary_key=True)
	    username = db.Column(db.String(80), unique=True)
	    email = db.Column(db.String(120), unique=True)

	    def __init__(self, username, email):
	        self.username = username
	        self.email = email

	    def __repr__(self):
	        return '<User %r>' % self.username



Der Tabellenname der Klasse kann folgendermaßen explizit angegeben werden::

	class User(db.Model):
		__tablename__ = 'my_table_user'
		...


