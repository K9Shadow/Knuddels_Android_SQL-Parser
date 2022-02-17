# knuddelsparser
SQL Parser für die Knuddels Android App v5.92


Moin,

bei dem Parser handelt es sich um ein SQL Script. Um verwertbare Daten zu bekommen müsst ihr das Script in einem Datenbank SQL Tool einlesen.
DB Browser könnt ihr beispielsweise nutzen. Dann speichert ihr das Ergebnis in eine CSV  Datei, welche ihr dann wiederum mit Excel einladet. In Excel könnt ihr dann nach Chats, usw. filtern.

Eure Knuddels Datenbank (com.knuddels.android/db/kunddels$USERNAME) im DB Browser öffnen.

Unter "SQL ausführen" das hier zur Verfügung gestellte Script einladen und ausführen.

Die erhaltenen Daten dann als CSV mit den Standardeinstellungen nach CSV exportieren (Haken rein bei "Spaltennamen in der ersten Zeile, Feld-Seperator ist das Komma und das String-Zeichen sind die Anführungsstriche. Das Zeilenumbruchs-Zeichen ist Windows CR+LF)

In Excel (2016) eine leere Arbeitsmappe auswählen. Unter "Daten" dann "Neue Abfrage", "Aus Datei", "Aus CSV" und eure exportierte *.csv auswählen.
Im nächsten Fenster Dateiursprung: 65001: Unicode (UTF-8), Trennzeichen Komma und Datentypenerkennung auf den ersten 200 Zeilen belassen und auf "Laden" unten rechts klicken.

Die Daten sollten nun mit vernünftigen Spalten und Zeilen angezeigt werden. Wenn nicht, ist etwas beim Import in Excel oder beim CSV-Export schiefgegangen.

Sollten jetzt bei den Überschriften noch keine "Sortierfunktion" zur Verfügung stehen auf "Start", "Sortieren und Filtern" und "Filtern" ankicken.

Thx an Rosi für Bugmeldungen. :)

