Hier ist ein "Template-Set" mit kommentierten Beispielen. Diese Vorlagen können direkt in AsciiDoc-Dokumenten kopiert und an die Bedürfnisse angepasst werden.

---

### A) Vorlagen für Block-Bilder (`image::`)

Verwenden Sie diese für alle Standardabbildungen, Diagramme und Fotos.

#### A.1: Das Minimal-Setup (Absolutes Muss)
Das Wichtigste ist der Alt-Text für die Barrierefreiheit.

```asciidoc
// --- A.1: Minimal-Setup für Block-Bilder ---
// Enthält nur das Nötigste: den Pfad und den alternativen Text.

image::pfad/zum/bild.png[Ein prägnanter, beschreibender Alt-Text]
```

#### A.2: Das Standard-Bild mit Größenkontrolle (90% der Fälle)
Die beste Methode, um die Größe zu steuern und einen optionalen Tooltip hinzuzufügen.

```asciidoc
// --- A.2: Standard-Bild mit Größenkontrolle und Tooltip ---
// Die benannten Attribute `alt`, `width` und `title` sind selbsterklärend und robust.

image::pfad/zum/bild.png[alt="Beschreibung für Screenreader", width=600, title="Dieser Text erscheint als Tooltip"]
```

#### A.3: Die formale Abbildung mit Titel und ID
Für wissenschaftliche Arbeiten, Dokumentationen oder wenn Sie auf das Bild verweisen möchten.

```asciidoc
// --- A.3: Formale Abbildung mit Titel und ID ---
// Der Punkt am Anfang erzeugt einen Block-Titel (Bildunterschrift).
// Die ID in doppelten eckigen Klammern ermöglicht Querverweise.

[[fig-architektur]]
.Abbildung 1: Die Systemarchitektur im Überblick
image::diagramme/architektur.png[alt="Diagramm der Systemarchitektur", width="80%"]
```
*Querverweis im Text:* `Siehe <<fig-architektur>> für eine visuelle Darstellung.`

#### A.4: Bild mit Textumfluss (Floating)
Nützlich für Layouts im Magazin-Stil.

```asciidoc
// --- A.4: Bild mit Textumfluss ---
// `float` lässt das Bild nach links oder rechts schweben, der Text fließt darum herum.
// `role` kann für zusätzliches CSS-Styling (z.B. einen Rand) genutzt werden.

image::portraits/autor.jpg[alt="Foto des Autors", width=200, float="right", role="img-bordered"]
```

#### A.5: Klickbares Bild (Link)
Macht das Bild zu einem Link, der sich optional in einem neuen Tab öffnet.

```asciidoc
// --- A.5: Klickbares Bild (Link) ---
// `link` enthält die Ziel-URL.
// `window="_blank"` öffnet den Link in einem neuen Tab/Fenster.

image::logos/projekt-logo.svg[alt="Projekt-Logo", width=250, link="https://projekt-homepage.com", window="_blank"]
```

#### A.6: Das "Cross-Media"-Bild (HTML & PDF optimiert)
Die Profi-Methode, um für verschiedene Ausgabeformate unterschiedliche Größen zu definieren.

```asciidoc
// --- A.6: "Cross-Media"-Bild für HTML & PDF ---
// `width` wird vom HTML-Konverter verwendet (Prozent ist gut für responsive Webseiten).
// `pdfwidth` wird vom PDF-Konverter verwendet (feste Einheiten wie `in` oder `%` der Textbreite sind hier besser).

image::screenshots/ui-feature.png[alt="Screenshot des neuen Features", width="90%", pdfwidth="100%"]
```

---

### B) Vorlagen für Inline-Bilder (`image:`)

Verwenden Sie diese nur für sehr kleine Symbole oder Icons direkt im Text.

#### B.1: Das einfache Icon
Ein kleines Icon im Fließtext mit Alt-Text.

```asciidoc
// --- B.1: Einfaches Inline-Icon ---
// Das Icon wird in seiner Originalgröße eingefügt.

Bitte speichern image:icons/save.svg[Speichern] Sie Ihre Änderungen.
```

#### B.2: Icon mit angepasster Größe
Die häufigste Anwendung: die Größe des Icons an die Schriftgröße anpassen.

```asciidoc
// --- B.2: Inline-Icon mit angepasster Größe ---
// `width` sollte auf einen kleinen Pixelwert gesetzt werden, um die Zeilenhöhe nicht zu sprengen.

Achtung image:icons/warning.svg[Warnung, width=16], dieses Feld ist ein Pflichtfeld!
```

---

### C) Anti-Pattern (Was man vermeiden sollte)

#### C.1: Bildproportionen verzerren
Vermeiden Sie es, Höhe und Breite manuell zu setzen, es sei denn, Sie wissen genau, was Sie tun.

```asciidoc
// --- ANTI-PATTERN: Bild verzerren ---
// Das Bild wird auf 800x200 Pixel gequetscht, was schrecklich aussieht.
// Lassen Sie das `height`-Attribut weg, damit der Browser die Proportionen beibehält.

// SCHLECHT:
image::landschaft.jpg[alt="Landschaft", width=800, height=200]

// BESSER:
image::landschaft.jpg[alt="Landschaft", width=800]
```

#### C.2: Riesige Inline-Bilder
Ein Inline-Bild (`image:`) sollte niemals groß sein.

```asciidoc
// --- ANTI-PATTERN: Riesiges Inline-Bild ---
// Dies wird die Textzeile auf 150 Pixel Höhe aufblähen und das gesamte Layout zerstören.
// Verwenden Sie stattdessen `image::` (zwei Doppelpunkte).

// SCHLECHT:
Der Bericht zeigt die folgenden Ergebnisse image:grosses-diagramm.png[Diagramm, width=150].

// BESSER (als eigener Block):
Der Bericht zeigt die folgenden Ergebnisse:
image::grosses-diagramm.png[Diagramm, width=150]
```

Dieses Template-Set sollte Ihnen eine solide Grundlage für praktisch jeden Anwendungsfall im Umgang mit Bildern in AsciiDoc bieten.