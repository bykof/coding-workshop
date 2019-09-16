<style>
.reveal code {
  background: lightgray;
  padding: 5px;
}
</style>

# HTML

*Hyptertext Markup Language*

---

HTML beschreibt die Struktur und Daten auf einer Webseite.

---

HTML besteht aus Elementen und wird mit einer XML ähnlichen Sprache beschrieben.

HTML ist __keine__ Programmiersprache. Es ist eine "Auszeichnungssprache".

----

XML Sprache

(einfaches Beispiel)

```xml
<element attribut-a="wert" />
```

----

XML Sprache

(verschaltetes Beispiel)

```xml
<element attribut-a="wert1" attribut-b="wert2">
  <kinder-element kinder-attribut="kinder-attribut">
    Text
  </kinder-element>
</element>
<element attribut-a="wert3" />
```

---

HTML Sprache

----

Ein HTML Dokument besteht immer aus folgenden "Elementen".
Elemente haben alle eine Bedeutung und Funktion die festgelegt wurde.

```html
<html>
  <head></head>
  <body></body>
</html>
```

---

### HTML __\<head\>__ Element

dient dazu "Metainformationen" über das Dokument auszuzeichnen.

Elemente im \<head\> Element sind __nicht__ direkt sichtbar!

----

### \<title\>

Beschreibt den Titel des Dokuments. Oben in der Navigationsleiste im Browser.

```html
<head>
  <title>Titel dieser Webseite</title>
</head>
```

----

### \<meta\>

Beschreiben die Metadaten für Suchmachinen und Browser.

```html
<head>
  <meta
    name="description"
    content="Lorem ipsum."
  />
  <meta
    name="keywords"
    content="Stichwort 1, Stichwort 2, Stichwort 3"
  />
  <meta
    name="author"
    content="Autorenname"
  />
</head>
```

----

### \<link\>

Bindet fremde Dokumente in die HTML Datei ein.
Wird hauptsächlich für externe CSS Stylesheets benutzt.

```html
<head>
  <link rel="stylesheet" type="text/css" href="theme.css">
</head>
```

----

### \<script\>

Bindet Code einer Skriptsprache ein. Bspw. Javascript

```html
<head>
  <script type="text/javascript">
  ...
  <script>
  <script type="text/javascript" src=".../index.js"></script>
</head>
```

----

### \<style\>

Enthält CSS Auszeichnungen

```html
<head>
  <style>
    ...
  </style>
</head>
```

----


Ein Beispiel:

```html
<html>
  <head>
    <title>Titel dieser Webseite</title>
    <meta
      name="description"
      content="Beschreibung der Webseite für Google."
    />
    <script>...</script>
    <style>...</style>
  </head>
</html>
```

---

### HTML __\<body\>__ Element

dient dazu die Rohdaten der Webseite anzuzeigen.
Design und Funktion von Rohdaten werden dann von __CSS__ und __HTML__ manipuliert.

----

Bei HTML Elementen unterscheidet man zwischen:

* Block Elementen
* Inline Elementen

----

### Block Elemente

erzeugen einen Block in dem ein Inhalt untergebracht wird.

----

### Inline Elemente

unterbrechen nicht den Textfluß.

----

Beispiel:

```html
<p> <!-- Blockelement -->
  <b>Fette<b> Schrift <!-- Inlineelement -->
</p>
```

Resultat:
<p><b>Fette</b> Schrift</p>

---

## Die verschiedenen \<body> Elemente

----

### Überschriften \<h1>

```html
<h1>Überschrift 1</h1>
<h2>Überschrift 2</h2>
<h3>Überschrift 3</h3>
<h4>Überschrift 4</h4>
<h5>Überschrift 5</h5>
<h6>Überschrift 6</h6>
```

----

Resultat:
<h1>Überschrift 1</h1>
<h2>Überschrift 2</h2>
<h3>Überschrift 3</h3>
<h4>Überschrift 4</h4>
<h5>Überschrift 5</h5>
<h6>Überschrift 6</h6>

----

### Paragraph \<p>
```html
<p>
  <b>Lorem</b> ipsum dolor sit amet, <u>consetetur</u> sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna <i>aliquyam erat</i>, sed diam voluptua.
</p>
```

Resultat:
<p>
  <b>Lorem</b> ipsum dolor sit amet, <u>consetetur</u> sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna <i>aliquyam erat</i>, sed diam voluptua.
</p>

----

### Bilder \<img>

```html
<img src="google.de/image.png" width="250" />
```

Resultat:
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/2000px-HTML5_logo_and_wordmark.svg.png" width="250" />

----

### Links \<a href="">

```html
<a href="http://google.com/">Linktext</a>
```

Resultat:
<a href="google.com">Linktext</a>

----

### Listen \<ul> - \<li>

```html
<ul>
  <li>Milch</li>
  <li>Zucker</li>
  <li>Eier</li>
</ul>
```

Resultat:
<ul>
  <li>Milch</li>
  <li>Zucker</li>
  <li>Eier</li>
</ul>

----

### Tabelle \<table> - \<tr> - \<td>

```html
<table>
  <tr><td>Vorname</td><td>Nachname</td><tr>
  <tr><td>Michael</td><td>Bykovski</td><tr>
</table>
```

Resultat:
<table>
  <tr><td>Vorname</td><td>Nachname</td><tr>
  <tr><td>Michael</td><td>Bykovski</td><tr>
</table>

----

### Das Div Element [Link](https://developer.mozilla.org/de/docs/Web/HTML/Element/div)
ist ein Inlineelement, was im Grunde keine Eigenschaften besitzt.
Es ist dazu da, später bestimmte Elemente zu gruppieren und durch CSS und JS der Gruppe Eigenschaften zu verleihen.

```html
<div>
  <p>Inhalt</p>
</div>
```

---

## Alles zusammen

----

```html
<html>
  <head>
    <title>Titel der Webseite</title>
  </head>
  <body>
    <h1>Dies ist eine Überschrift</h1>
    <p>Dies ist ein Paragraph</p>
    <hr>
    <h2>Dies ist eine Überschrift</h2>
    <p>Dies ist ein Paragraph</p>
    <img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome.png" width="200px">
  </body>
</html>
```

[Resultat](https://jsfiddle.net/n8jxvtaw/)

---

> In der Informatik gibt es nichts, was nicht dokumentiert ist.

[SelfHTML Link](https://wiki.selfhtml.org/wiki/Schnell-Index/HTML)
