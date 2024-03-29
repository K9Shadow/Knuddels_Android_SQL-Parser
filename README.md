# knuddelsparser

WICHTIGES UPDATE: AB Version 6.7.3 (Oktober 2023) hat Knuddels eine Änderung in der Architektur vorgenommen. Chats werden nicht mehr im Dateisystem von Android gespeichert! Sobald der Ordner com.knuddels.com/database/ vorhanden ist, sind keine Chats mehr lokal gespeichert.

SQL Parser für die Knuddels Android App (getestet an Datenbanken aus v5.92, v6.37 (Danke Rosi) und v6.79 (Danke an Malte IZ)).

Die geparsten Daten sind verifiziert. Habe mich selbst bei Knuddels registriert und die App mit eigenen Chats unter die Lupe genommen.
Der Parser bereitet Daten aus privaten Chats auf. Besuchte öffentliche Kanäle und öffentliche Chats in den Kanälen werden NICHT aufbereitet.


Moin,

bei dem Parser handelt es sich um ein SQL Script. Um verwertbare Daten exportieren zu können, müsst ihr das Script in einem SQL Datenbank Tool einlesen.
Ihr könnt beispielsweise DB Browser nutzen. Anschließend speichert ihr das nach dem Ausführen des Scripts gespeicherte Ergebnis als CSV-Datei ab, welche ihr dann wiederum mit Excel einladet. In Excel könnt ihr dann nach Chats, Usern, Datum, usw. filtern.

Schritt-für-Schritt-Anleitung:

Eure Knuddels Datenbank (com.knuddels.android/db/kunddels$USERNAME) im DB Browser öffnen.

Unter "SQL ausführen" das hier zur Verfügung gestellte Script einladen und ausführen.

Die erhaltenen Daten dann als CSV mit den Standardeinstellungen nach CSV exportieren (Haken rein bei "Spaltennamen in der ersten Zeile, Feld-Seperator ist das Komma und das String-Zeichen sind die Anführungsstriche. Das Zeilenumbruchs-Zeichen ist Windows CR+LF)

In Excel (2016) eine leere Arbeitsmappe öffnen. Unter "Daten" dann "Neue Abfrage", "Aus Datei", "Aus CSV" und eure exportierte .csv auswählen (oder einfach "Daten" "Text in Spalten".
Im nächsten Fenster Dateiursprung: 65001: Unicode (UTF-8), Trennzeichen Komma und Datentypenerkennung auf den ersten 200 Zeilen belassen und auf "Laden" unten rechts klicken.


Die Daten sollten nun mit vernünftigen Spalten und Zeilen und richtigen Sonderzeichen angezeigt werden. Wenn nicht, ist etwas beim Import in Excel oder beim CSV-Export schiefgegangen.

Sollten jetzt bei den Überschriften noch keine "Sortierfunktion" zur Verfügung stehen in Excel auf "Daten", "Sortieren und Filtern" und "Filtern" klicken.

Ursprungscode: Niklas Linder, 17.09.21 :)

Codeupdate: 17.02.22 - Thx an Rosi für die Bug- und Verbesserungsmeldungen. :)

Codeupdate 2: 19.09.22 - Thx an Malte aus IZ für Rückmeldung. Die UserID sollte nun die einmalige UserID sein. Die zuvor geparste ID war nicht einzigartig.

Update 3: 17.10.23 - Mit Knuddelsversion 6.7.3 werden keine Chats mehr lokal im Gerät gespeichert. - Thx an Andre. :)


Wer noch Verbesserungsvorschläge hat, bitte melden! Das Ganze ist wip.
