=======
Notizen
=======

Grundlagen HTML
---------------

HTML ist für den Inhalt zuständig
"""""""""""""""""""""""""""""""""

Grundstruktur
^^^^^^^^^^^^^

======== ===============================
<html>        Das gesamte HTML-Dokument
<head>        Kopfdaten
<body>        Der anzuzeigende Inhalt
======== ===============================

Kopfdaten
^^^^^^^^^
======== =================================================================
base      Basis für relative Verweise
link      Beziehungen zu anderen Dokumenten im Web-Space 
meta      Angaben, die die Verwaltung des Dateiinhalts erleichtern sollen
style     Stylesheet-Angaben
title     Titel der Seite (wird in Regsitern/Tabs angezeigt)
======== =================================================================

Textstrukturierung
^^^^^^^^^^^^^^^^^^
============ =========================================
<h1> - <h6>   Überschriften 1. - 6. Ordnung
<p>           Textabsätze
<div>         gruppierendes Element
<ul>          ungeordnete Liste
<ol>          geordnete Liste
<li>          Elemente von *ol* bzw. *ul*
<hr>          thematischer Bruch / horizontale Linie
============ =========================================

Textauszeichnung
^^^^^^^^^^^^^^^^
============ ======================================================
<a>           Verweise (Hyperlinks)   
<b>           hervorgehobener Text, üblicherweise fett dargestellt
<em>          hervorgehobener Text
<i>           üblicherweise kursiv dargestellt
<u>           üblicherweise unterstrichen dargestellt
<strong>      besonders wichtige Informationen
<q>           Zitat im Fließtext
<br>          expliziter Zeilenumbruch
============ ======================================================

Tabellen
^^^^^^^^
============ =========================================
<table>       
<tr>          Tabellezeile
<td>          Tabellenspalte (Datenfelder)
<th>          Kopffelder
============ =========================================




<html> and <body> = alles auf einer Webseite muss zwischen <html> und </html>
stehen. Der eigentlich Text steht im zwischen <body> und </body>

<!DOCTYPE html> = steht ganz am Anfang und sagt dem Browser welche Version von
HTML genutzt wird. Und hat keinen END-TAG.
Beispiel:
<!DOCTYPE html>
<html>
  <body>
    <h1>Web Development.</h1>
    <p>We´re learning HTML</p>
  <body>
<html>

<div> = The outer <div class="nav">..</div> groups the elements into the
navigation bar section of the web page. The inner <div class="container">..</div>
wraps the contents in a container.
We'll use both classes in the next section to style the navigation bar.



Grundlagen CSS
--------------
CSS ist für das Design zuständig
""""""""""""""""""""""""""""""""

Farbe ändern:
h1 {
    color: red;
}
Zuerst muss man den jeweligen Bereich auswhälen (h1)  und in der geschwungenen
Klammer kommt wie h1 aussehen soll

class selector (div CLASS="HEADER")
kann durch einen "." ersetzt werden = .header

.header p = wählt alle p elemente aus und färbt diese um

Um die farben zu ändern kann man entweder RGB Werte oder Hexdezimalzahlen verwenden.
RGB Werte gehen von 0 bis 255 {rgb(125,33,0)}
Hexadezimalhzahlen von 00 bis ff (#9933CC)

Font Family
1.font family:Arial,Helvetica,sans-serif;
2.font family:"Times New Roman", Times, serif;
3.font family:"Courier New", Courierm monosüace;

Größe
die größe kann in Pixel, ems und rems gemessen werden

Hintergrundfarbe
z.B: .jumbotron {
        background-color: #0099cc
}

Hintergrundbild
z.B: .jumbotron {
        background-image:
        url('http://goo.gl/ODpi3y')
}

Rahmen + Padding (abstangen zwischen rahmen und Text) + margin (größe des rahmens)
z.B: .jumbotron h1 {
        padding: 23px;
        border: 3px solid #cc0000;
        margin: 14px;
}


<html>
  <head>
   <link href="maik.css" rel="stylescheet"/>
  </head>
  <body>
   ..........
"Link" sagt dem Browser wo man die Css Datei "stylen" kann
"rel" sagt dem browser das die Datei eine Verknüfung ist
"href" für zu der CSS Datei


Display
.nav li {
  display: block;
}
Block elemente : h1, p, ul, li
Inline elemente: img, a

Position
.jumbotron h1 {
  position: fiexed;
  top: 30px;
  right: 5px;
  left: ..;
  bottom: ..;
}

Float:
bewegt das Element ganz links oder ganz rechts auf die Seite
img {
  float: right;
}

Grid (gitter)
<div class="row">

  <div class="col-md-6">
    <h4>Content 1>/h4>
  </div>

  <div class="col-md-6">
    <h4>Content 2</4>
  </div>

  </div>

.row ist da um eine horizontale Gruppe zu erstellen
  .com-md-6 damit werden 6 Spalten gebildet


Tabs
  <ul class="nav nav-tabs">
	<li><a href="#">Primary</a></li>
	<li class="active"><a href="#">Social</a></li>
	<li><a href="#">Promotions</a></li>
	<li><a href="#">Updates</a></li>
</ul>

Pils (tasten)
<ul class="nav nav-pils">
<li><a href="#">Primary</a></li>
<li class="active"><a href="#">Social</a></li>
<li><a href="#">Promotions</a></li>
<li><a href="#">Updates</a></li>
</ul>

Jumbotron
wird verwendet um zusätzliche Aufmerksamkeit zu den wichtigen Inhalten aufzurufen

<div class="jumbotron">
	<h1>Find a place to stay.</h1>
	<p>Rent from people in over 34,000 cities and 192 countries.</p>
</div>

Comment (kommentar)
<!-- comment -->
ODER
/*   comment */


Bild 
<img src=“url von dem Bild”></img>

Bild mit Link
<a href="https://www.google.de/search?q=new+york+skyline&source=lnms&tbm=isch&sa=X&ei=mc4GVJjtNNCPNqX0gdgC&sqi=2&ved=0CAYQ_AUoAQ&biw=1920&bih=898">

<img src="http://www.hdwallpapers.in/walls/new_york_skyline-wide.jpg"/>
</a>


Tabellezeile
<table>

<thead>

<th colspan="2"></th>

<tr>
  <th>Text</th> (fett geschrieben)
</tr>


</thead>

   <tr>
     <td>One</td>
     <td>10</td>
   </tr>

   <tr>
     <td>Two</td>
   </tr>


</table>

TR=Zeilen
TD=spalte


Div (in Stücke aufteilen) & Span (styling für kleine Sachen)

<div style="background-color:yellow"></div>
<p>hallo das ist <span sytle=“ color:red”>nur</span> ein Beispiel</p>

Link 
<link type="text/css" rel="stylesheet" href="stylesheet.css"/>


a:link: ein umbesuchter link.
a:visited: ein besuchter link.
a:hover: ein link wo die Mauser darüber ist



Nth child
p:first-child {
 font-family: cursive;
}

p:nth-child(2) {
 color:#CC0000;   
}

p:nth-child(4) {
 color:#00FF00;   
}

p:nth-child(5) {
 font-size:22px;   
}

Wenn nicht alle Paragraphen umgefärbt werden soll geht dann mit dem Wähler ntht-child


