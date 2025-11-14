# Mitwirkung an dem Joomlabuch

## Lizensierung

Wenn Du einen Pull Request eröffnest, erklärst Du Dich damit einverstanden, Deine Arbeit unter der [Projektlizenz](LICENSE.asc) zur Verfügung zu stellen.

## Ein Problem (issue) melden: Rechtschreibung, Gramatik oder Fehler.

Suche zuerst nach ähnlichen Problemen, bevor Du ein neues Problem erstellst.

Wenn dieses Problem auf der Website joomlabuch.de entdeckt wurde, überprüfe bitte, ob das Problem auch in der PDF-Version vorhanden ist.
Möglicherweise wurde das Problem bereits in den Quelldateien behoben, aber noch nicht auf der Website veröffentlicht.

## Kleine Korrekturen

Errata und grundlegende Klarstellungen werden akzeptiert, wenn wir uns einig sind, dass sie den Inhalt verbessern.
Du kannst auch ein Problem melden, damit wir besprechen können, wie oder ob das Problem behoben werden muss.

## Umfangreiche Überarbeitungen

Eröffne eine Diskussion, bevor du beginnst.
Eine umfangreiche Überarbeitung ist in der Regel sehr subjektiv und dient oft nur der Klarstellung für eine kleine Anzahl von Lesern.
Es ist unwahrscheinlich, dass deine Prosa *so* viel besser ist, dass es sich lohnt, große Teile des Textes zu ändern.

## Dateinamen und organisation der Inhalte

Alle Texte befinden sich im book Verzeichnis, darin gibt es für jedes Kapitel ein Verzeichnis in der Form Kapitelnummer, minus, Name des Kapitels. In diesem, Verzeichnis gibt es dann eine Datei mit dem gleichen Namen als ".adoc". Die Texte sind im AsciiDoc Format geschrieben. Kapitel haben eine Level zwei Überschrift, für den dritten Level werden dann einzelne Dateien im Verzeichnis abschitte angelegt, diese starten auf wieder mit einer Nummer, minus, Name des Bereichs. Beispiele:
* book/15-spezielle-erweiterungen
* book/15-spezielle-erweiterungen/15-spezielle-erweiterungen.adoc
* book/15-spezielle-erweiterungen/abschnitte/01-shop-systeme.adoc

Es ist auch erlaubt bei sehr kurzen Kapiteln die Strukturierung zu vereinfachen oder auch bei langen Kapiteln zu erweitern. Wie wollen das nicht übertreiben, aber es soll ein abgeschlossener Themenbereich sein. Das soll die Zusammenarbeit erleichtern. 

## Bilder

Alle Bilder sind im media Verzeichnis nach Kapiteln sortiert. Sprich alle Bilder aus Kapitel 13 sind in media/13. 

## Nummern
Alle Nummern bei Dateinamen und Bildern sind immer zweistellig ggf. mit einer führenden Null.
Falsch: 1-einleitung, 7.png
Richtig: 01-einleitung, 07.png

## Rahmen
* Fokus sind Joomla-Anfänger z.B. eine Redakteurin.
* Wir verwenden die Du-Form.
* Wir dokumentieren Joomla! Version 6.
* Wir gendern in der Form: Administrator:innen.

## Danke

Vielen Dank an https://github.com/progit/progit2 das git-scm book hat uns das aufsetzen sehr erleichtert und uns sicher Stunden an research erspart.
