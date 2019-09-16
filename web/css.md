<style>
.reveal code {
  background: lightgray;
  padding: 5px;
}
</style>

# CSS

Cascading Style Sheets

---

## CSS

styled alle HTML Elemente und ihre Inhalte.

---

## Aufbau

Der Aufbau von CSS wurde nur für CSS erfunden. Es gibt somit keine ähnliche Auszeichnungssprache, die CSS gleicht.

----

### Syntax

```css
Selektor1 [, Selektor2 [, …] ] {
    Eigenschaft-1: Wert-1;
    …
    Eigenschaft-n: Wert-n[;]
}
```

----

### Beispiel

```css
.first-text {
  font-size: 14px;
  font-weight: bold;
}
```

---

## Selektoren

Selektoren in CSS "selektieren" Elemente im HTML und fügen diesen ein Styling hinzu.

[Link](https://de.wikipedia.org/wiki/Cascading_Style_Sheets)

----

### Einfache Selektoren

|Selektor|Funktion|
|--------|--------|
|`*`|Jedes Element|
|`E`|Jedes Element mit Elementnamen `E`|
|`.c`|Jedes Element mit Attribut `class='c'`|

----

|Selektor|Funktion|
|---|----|
|`#myid`|Das Element mit Attribut `id='myid'`|
|`[foo='bar']`|Jedes Element, deren Attribut `foo` mit dem Wert `bar`|

----

### Kombinatoren

|Kombinator|Funktion|
|----------|--------|
|E F|Alle Elemente F, die Nachfahren von E sind|
|E > F|Alle Elemente F, die ein Kind des Elements E sind|

----

### Beispiel

```css
p i {
  color: blue;
}
p > i {
  color: red;
}
```
```html
<p>
  <i>Kind</i>
  <span><i>Nachfahre</i></span>
</p>
```

[Resultat](https://jsfiddle.net/god2cm6z/2/)

----

### Pseudoklassen

Fangen immer mit `:` an.

|Pseudoklasse|Funktion|
|---|---|
|:hover|das Element, über dem sich der Mauszeiger befindet|
|:first-child|Element, welches das erste Kindelement ist|
|::first-letter|erstes Zeichen|

----

Beispiel:

```css
a:hover {
  font-decoration: line-through;
}
```

[Beispiel](https://jsfiddle.net/wdv4o1zh/)

---

## CSS Eigenschaften

[Link](https://wiki.selfhtml.org/wiki/CSS/Eigenschaften)

----

Es gibt verschiedene Eigenschaften die durch einen `Selektor` auf einem Element angewendet werden können.

----

`Eigenschaften` besitzen einen `Namen` und einen `Wert`, wobei der Wert verschiedene `Typen` haben kann.
[Link](https://wiki.selfhtml.org/wiki/CSS/Wertetypen/Zahlen,_Ma%C3%9Fe_und_Ma%C3%9Feinheiten)

Note:
  - Gehe die Einheiten in dem Link durch.

----

### Texteigenschaften

```css
p {
  color: #32a852;
  letter-spacing: 0.25em;
  font-size: 16px;
  font-stretch: extra-expanded;
}
```

[Resultat](https://jsfiddle.net/q4je3km7/)

----

### Abstandseigenschaften

```css
.big-spacing {
  margin: 20px;
  padding-top: 30px;
  padding-left: 20px;
  width: 200px;
  height: 200px;
  border: 3px solid black;
}
```

[Resultat](https://jsfiddle.net/0qwgy1rf/)

----

### Positionierung
- `static` - statisch
  - Inhalte folgen linear nacheinander, so wie sie im HTML-Dokument einander folgen.
- `relative` - relativ
  - Zunächst nicht anders als static.
- `absolute` - absolut
  - Das Element wird aus dem linearen Fluß genommen, sein ursprünglicher Raum kollabiert.

----

- `fixed` - fest
  - Wie absolut, aber das Koordinatensystem des fixierten Elements ist der Viewport, nicht mehr das Dokument. Das Element wird nicht mehr mit dem Dokument gescrollt.
- `sticky` - festgesteckt
  - Wie fixed, aber das Element scrollt bis zu einem vorgegebenen Punkt und bleibt dann im Viewport fixiert
- `inherit` - vererbt
  - Das Element erbt die Art der Positionierung von seinem umfassenden Element.

----

[Beispiele](https://www.w3schools.com/css/css_positioning.asp)

---

## CSS-Box-Modell

![css-box-modell](https://upload.wikimedia.org/wikipedia/commons/7/7a/Boxmodell-detail.png)

---

Weiter gehts mit Javascript...
