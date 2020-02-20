# M426_Formen_Finden

Unserer Team baut eine Software für das Suchen von doppelten geometrischen Formen. Diese werden verwendet um bei der Verpackung Kosten zu sparen.

Nihal Singh Singh, Mike Krenn, Leyton Tomio, Annina Blum und Adrian Michel

------------------------------------------------------------------------------------------------

Modul 426: Projektbeschreibung

• Die Gruppen sind organisiert und können auf eine funktionierende Infrastruktur zurückgreifen • Das Projekt ist verstanden und die Planung kann starten • Das Bewertungsraster ist bekannt und nachvollziehbar

Checkliste Infrastruktur

Lizenziertes Visual Studio Enterprise auf bmWP2 (oder eigenem Rechner)
Sicherung der VM für den Fall der Fälle (1x auf smartlearn selber, 1x extern)
Zugang auf den Team Foundation Server per Browser
Zugang auf den Team Foundation Server per Visual Studio
Beschreibung des Projekts

Ihr Team baut eine Software für das Suchen von doppelten geometrischen Formen. Diese werden verwendet um bei der Verpackung Kosten zu sparen. Das strategische Ziel des Auftraggebers ist es mit der Software langfristig Kosten zu sparen, weil Verpackung ähnlicher Formen viel schneller geht.

In der Produktion werden im Parallelbetrieb laufend neue Formen erstellt, diese werden in grösseren Mengen in eine Grafik eingescannt.
Die Umstellung des Verpackungsroboters auf eine neue Form dauert eine Weile, deshalb sollen gleiche Formen erkannt werden.
Die zu analysierenden Formen werden in einer .bmp Datei angeliefert. Diese beinhaltet schwarze und weisse Punkte, welche mehrere Formen darstellen. Die maximale Grösse einer Grafik wird 768 x 768 Pixel sein. Zur Entwicklung werden mehrere Grafiken zur Verfügung gestellt, das Entwicklerteam kann diese auch selber herstellen um eigene Fälle zu testen. (Anhang A Erstellung von Testgrafiken) Als Output soll nebst der grafischen Darstellung auch eine Textdatei erstellt werden, in welcher die Gruppen und die Anzahl gleicher Formen gespeichert ist. (Anhang B Formen-Skript .for) Am Ende des 2. Sprints werden die Programme alle Gruppen gegeneinander antreten!

Software mit agilen Methoden entwickeln 2/3 Projektbeschreibung

Modul 426 Reto Glarner AB426-05 HS 2018

Anforderungen an das Programm

Wichtigkeit hoch

Eine Form kann einmalig, doppelt oder mehrfach vorkommen
Gleiche Form bedeutet auch gleiche Grösse
Mehrfache Formen sollen auf dem Bildschirm angezeigt werden (Nummerierung, Einfärbung,
Einrahmung usw. möglich)

Der Benutzer kann interaktiv neue Grafiken zur Analyse auswählen
Die Kennzahlen werden in eine Textdatei ausgegeben (Anhang B Formen-Skript .for)
Wichtigkeit mittel

Die Berechnung sollte nicht länger als 10 Sekunden dauern
Während der Berechnung wird der Fortschritt der Berechnung visualisiert
Die Formen werden auch erkannt wenn dies um 90°, 180° oder 270° rotiert vorkommen
Der Name der Ausgabedatei kann durch den Benutzer definiert werden
Das Programm kann mit Formen umgehen, welche als Umriss dargestellt sind
Wichtigkeit tief

Das Programm soll während der Berechnung ansprechbar sein
Das Programm soll mit farbigen Formen zurechtkommen
Das Programm erkennt, wenn es sich um Rechtecke, Dreiecke und Kreise handelt
Falls Sie noch weitere Fragen zu den Anforderungen haben, wird die Lehrperson die Rolle des Kunden übernehmen.

Technische Vorgaben

Die technischen Vorgaben sind unveränderbar und bieten keinen Raum für Interpretation.

Es soll eine Desktop Applikation (.exe) für Windows Rechner erstellt werden.
Als Programmiersprache wird C# eingesetzt.
Die Benutzerschnittstelle wird mittels WPF realisiert.
Das Programm darf nicht abstürzen.
Es können zu Testzwecken zusätzliche Fenster angezeigt werden (Logging usw.)
Es werden keine zusätzlichen Komponenten für Visual Studio installiert. (Ausnahme: Resharper)
Vorgaben zur Gruppenarbeit

Die Gruppen werden nicht verändert.
Bei Krankheit oder anderen Absenzen wird der Aufwand möglichst ausserhalb der Schule nachgeholt.
Alle Teammitglieder leisten gleich viel Aufwand. (Bei Unregelmässigkeiten kann die Lehrperson Einzelnoten vergeben)
Jedes Teammitglied trägt mindestens einmal pro Schulwoche den Projektfortschritt nach und synchronisiert seine Repository mit dem Server. (mindestens Pull)
Jedes Teammitglied legt fertige Tasks zeitnah auf dem Server ab.
Das Kopieren oder Abschreiben von Code ist generell untersagt. Kurze Passagen von maximal 10 Zeilen sind unter Angabe der Quelle erlaubt. Zuwiderhandlung führt zur Note 1.
Bei bewerteten Besprechungen (Daily Scrum Meeting, Sprint Review) und Teams >4 Personen kann jeweils pro Gruppe eine Person als Product Owner und eine als Scrum Master agieren. Formale Vorgaben (LB2 / LB3)
Jedes Dokument hat ein Deckblatt welches alle Namen des Teams, Klasse, Teamnummer und Datum enthält
Jede Seite trägt eine Seitenzahl und Dokumentname
Die Schriftarten sind einheitlich und alle Texte gut lesbar
Bildern werden ohne Qualitätsverlust angezeigt
Software mit agilen Methoden entwickeln 3/3 Projektbeschreibung

Modul 426 Reto Glarner AB426-05 HS 2018

Anhang A –Erstellung von Testgrafiken

Das Format für die Grafiken kann mit einem Grafikprogramm (zum Beispiel „mspaint.exe“) erstellt werden. Die Kantenlänge sollte immer ein Vielfaches von 4 Bytes sein. (32 Pixel, 64 Pixel usw.) Als maximale Grösse wird 768 x 768 Pixel in der Simulation vorkommen. Speichern Sie das Bild als Schwarz-Weiss (Monochrom) im Format BMP ab!

Für das korrekte Verarbeiten des BMP Formats finden Sie alle relevanten Informationen unter:

https://de.wikipedia.org/wiki/Windows_Bitmap 

Sie können auch einen Hex-Editor einsetzen um die BMP Datei zu analysieren. (zum Beispiel „XVI32.exe“)

Anhang B – Formen-Skript .for

Pro erkannte Form wird eine Zeile verwendet. Als Zellenbegrenzer dient das Semikolon ; Zelle 1 Eindeutiger Zähler 1 - ... zur Identifikation der Form Nur ganze Zahlen Zelle 2 Gruppennummer der Form Nur ganze Zahlen

Bsp.:

1;1 2;2 3;1 4;1
