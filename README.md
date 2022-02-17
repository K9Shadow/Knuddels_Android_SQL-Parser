# knuddelsparser
SQL Parser für die Knuddels Android App v5.92


Moin,

bei dem Parser handelt es sich um ein SQL Script. Um verwertbare Daten exportieren zu können, müsst ihr das Script in einem SQL Datenbank Tool einlesen.
Ihr könnt beispielsweise DB Browser nutzen. Anschließend speichert ihr das nach dem Ausführen des Scripts gespeicherte Ergebnis als CSV-Datei ab, welche ihr dann wiederum mit Excel einladet. In Excel könnt ihr dann nach Chats, Usern, Datum, usw. filtern.

Schritt-für-Schritt Anleitung:

Eure Knuddels Datenbank (com.knuddels.android/db/kunddels$USERNAME) im DB Browser öffnen.

Unter "SQL ausführen" das hier zur Verfügung gestellte Script einladen und ausführen.

Die erhaltenen Daten dann als CSV mit den Standardeinstellungen nach CSV exportieren (Haken rein bei "Spaltennamen in der ersten Zeile, Feld-Seperator ist das Komma und das String-Zeichen sind die Anführungsstriche. Das Zeilenumbruchs-Zeichen ist Windows CR+LF)

In Excel (2016) eine leere Arbeitsmappe öffnen. Unter "Daten" dann "Neue Abfrage", "Aus Datei", "Aus CSV" und eure exportierte *.csv auswählen.
Im nächsten Fenster Dateiursprung: 65001: Unicode (UTF-8), Trennzeichen Komma und Datentypenerkennung auf den ersten 200 Zeilen belassen und auf "Laden" unten rechts klicken.

Die Daten sollten nun mit vernünftigen Spalten und Zeilen und richtigen Sonderzeichen angezeigt werden. Wenn nicht, ist etwas beim Import in Excel oder beim CSV-Export schiefgegangen.

Sollten jetzt bei den Überschriften noch keine "Sortierfunktion" zur Verfügung stehen in Excel auf "Start", "Sortieren und Filtern" und "Filtern" klicken.

Thx an Rosi für Bugmeldungen. :)

