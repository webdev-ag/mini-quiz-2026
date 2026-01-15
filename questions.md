## HTML - Frage 1

Welche dieser Elemente gibt es in HTML?

```html
<paragraph>
<p>
<text>
<div>
```

---

## HTML - Lösung 1

**Existieren in HTML:**
- `<p>` ✓
- `<div>` ✓

**Existieren NICHT:**
- `<paragraph>` ✗
- `<text>` ✗

---

## HTML - Frage 2

Wozu ist das `<p>` Element?

---

## HTML - Lösung 2

Das `<p>` Element ist für **Paragraphen** (Absätze).

Es wird verwendet, um Textabsätze zu erstellen.

---

## HTML - Frage 3

Wie schreibe ich eine unsortierte Liste, die einen Punkt für jeden Eintrag hat?

---

## HTML - Lösung 3

```html
<ul>
  <li>Erster Punkt</li>
  <li>Zweiter Punkt</li>
  <li>Dritter Punkt</li>
</ul>
```

- `<ul>` = unordered list
- `<li>` = list item

---

## HTML - Frage 4

Wie sieht ein HTML Dokument aus?

---

## HTML - Lösung 4

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Meine Seite</title>
  </head>
  <body>
    <h1>Hallo Welt!</h1>
  </body>
</html>
```

---

## CSS - Frage 1

Was macht diese Anweisung?

```css
p {
  color: red;
}
```

Bei diesem HTML:
```html
<p>Text 1</p>
<div>Text 2</div>
<h1>Text 3</h1>
<h2>Text 4</h2>
<ul><li>Text 5</li></ul>
```

---

## CSS - Lösung 1

Nur die `<p>` Elemente werden **rot** gefärbt.

Die anderen Elemente (div, h1, h2, ul, li) bleiben unverändert.

---

## CSS - Frage 2

Was macht diese Anweisung?

```css
.b-red {
  border: 2px solid red;
}
```

Bei diesem HTML:
```html
<p>Erster Absatz</p>
<p class="b-red">Zweiter Absatz</p>
<p>Dritter Absatz</p>
```

---

## CSS - Lösung 2

Nur der **zweite Absatz** bekommt einen **2 Pixel dicken, roten Rahmen**.

Die anderen beiden Absätze haben keinen Rahmen.

---

## CSS - Frage 3

Was macht diese Anweisung?

```css
.bg {
  background-color: green;
}
```

Bei diesem HTML:
```html
<p class="pu">Was passiert mit diesem Text?</p>
<p class="bg">Hat dieser Text einen Hintergrund?</p>
<p class="ck">Was ist hiermit?</p>
```

---

## CSS - Lösung 3

Das mittlere `<p>` Element bekommt einen **dunkelgrünen Hintergrund**.

---

## CSS - Frage 4

Was macht diese Anweisung?

```css
.box {
  border: 1px solid black;
  width: 100px;
  height: 100px;
}
```

Bei diesem HTML:
```html
<div class="box"></div>
```

---

## CSS - Lösung 4

Es entsteht eine **quadratische Box**:
- Schwarzer Rahmen (1px)
- 100 Pixel breit
- 100 Pixel hoch

---

## JavaScript - Frage 1

Was macht diese Anweisung?

```javascript
const answer = window.prompt('Wie heißt du?');
window.alert(answer);
```

---

## JavaScript - Lösung 1

Es öffnet sich ein **Eingabefenster** mit der Frage "Wie heißt du?".

Die Eingabe des Nutzers wird in der Variable `answer` gespeichert und dann in einer Alert-Fenster angezeigt.

---

## JavaScript - Frage 2

Was macht diese Anweisung?

```javascript
const a = 5;
const b = 3;
window.alert(a + b);
```

---

## JavaScript - Lösung 2

Es öffnet sich ein **Alert-Fenster** mit dem Wert **8**.

Die beiden Zahlen werden addiert (5 + 3 = 8).

---

## JavaScript - Frage 3

Was gibt diese Anweisung wo aus?

```javascript
if (5 > 3) {
  console.log("A");
} else {
  console.log("B");
}
```

---

## JavaScript - Lösung 3

**Ausgabe:** `"A"` in der **Browser-Konsole**

Weil 5 größer als 3 ist, wird die if-Bedingung erfüllt.

---

## JavaScript - Frage 4

Was gibt diese Anweisung aus?

```javascript
for (let i = 0; i < 3; i = i + 1) {
  console.log('Runde ', i);
}
```

---

## JavaScript - Lösung 4

**Ausgabe in der Konsole:**
```
Runde 0
Runde 1
Runde 2
```

Die Schleife läuft 3-mal (i = 0, 1, 2).

---

## Gut gemacht! 🎉

Jetzt geht's weiter mit dem Game!