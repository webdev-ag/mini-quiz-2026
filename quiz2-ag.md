# JavaScript Quiz
## Web-AG – Grundlagen

---

## Frage 1

Was steckt in der Variablen `x`?
Welchen Datentyp hat die Variable `x`?

```js
let x = 42;
```

- A) `string` = Zeichenkette
- B) `float` = Kommazahl
- C) `number` = Zahl
- D) `integer` = Ganzzahl

---

## Antwort 1

✅ **C) `number`**

In JavaScript gibt es keinen Unterschied zwischen ganzen Zahlen und Kommazahlen – alles ist `number`.

---

## Frage 2

Was wird angezeigt?

```js
alert(3 + 4);
```

- A) `34`
- B) `7`
- C) `3 + 4`
- D) `"7"`

---

## Antwort 2

✅ **B) `7`**

Zwei Zahlen mit `+` werden addiert. Das Ergebnis `7` erscheint im Alert-Fenster.

---

## Frage 3

Was wird angezeigt?

```js
alert("3" + "4");
```

- A) `7`
- B) `"7"`
- C) `34`
- D) Fehler

---

## Antwort 3

✅ **C) `34`**

Beide Werte sind Strings (`"..."`) – `+` verbindet sie hier zu `"34"`.

---

## Frage 4

Was wird angezeigt?

```js
alert("Ich bin " + 15 + " Jahre alt");
```

- A) Fehler
- B) `Ich bin 15 Jahre alt`
- C) `Ich bin  Jahre alt`
- D) `NaN`

---

## Antwort 4

✅ **B) `Ich bin 15 Jahre alt`**

Wird eine Zahl mit einem String verbunden, wird die Zahl automatisch in einen String umgewandelt.

---

## Frage 5

Welchen Wert hat `ergebnis`?

```js
let ergebnis = "10" - 4;
console.log(ergebnis);
```

- A) `"104"`
- B) `6`
- C) `"6"`
- D) Fehler

---

## Antwort 5

✅ **B) `6`**

Bei `-` kann JS keinen String verbinden – es rechnet automatisch. `"10"` wird zur Zahl `10`, dann `10 - 4 = 6`.

---

## Frage 6

Was gibt dieser Code aus?

```js
let name = "Anna";
if (name === "Anna") {
  console.log("Hallo Anna!");
} else {
  console.log("Wer bist du?");
}
```

- A) `Wer bist du?`
- B) `Hallo Anna!`
- C) Beides
- D) Nichts

---

## Antwort 6

✅ **B) `Hallo Anna!`**

`name === "Anna"` ist `true`, deshalb wird der `if`-Block ausgeführt.

---

## Frage 7

Was gibt dieser Code aus?

```js
let alter = 10;
if (alter >= 18) {
  console.log("Erwachsen");
} else {
  console.log("Noch nicht!");
}
```

- A) `Erwachsen`
- B) `Noch nicht!`
- C) Nichts
- D) Fehler

---

## Antwort 7

✅ **B) `Noch nicht!`**

`10 >= 18` ist `false`, daher wird der `else`-Block ausgeführt.

---

## Frage 8

Was gibt dieser Code aus?

```js
for (let i = 0; i < 3; i++) {
  console.log(i);
}
```

- A) `1 2 3`
- B) `0 1 2 3`
- C) `0 1 2`
- D) `1 2`

---

## Antwort 8

✅ **C) `0 1 2`**

Die Schleife startet bei `0`, läuft solange `i < 3` gilt – also bis `i = 2`.

---

## Frage 9

Was gibt dieser Code aus?

```js
let farben = ["rot", "grün", "blau"];
for (let farbe of farben) {
  console.log(farbe);
}
```

- A) `0 1 2`
- B) `rot grün blau`
- C) `farbe farbe farbe`
- D) Fehler

---

## Antwort 9

✅ **B) `rot grün blau`**

`for...of` geht durch alle **Werte** eines Arrays – hier also die Farbnamen.

---

## Frage 10

Was gibt dieser Code aus?

```js
let farben = ["rot", "grün", "blau"];
for (let i in farben) {
  console.log(i);
}
```

- A) `rot grün blau`
- B) `0 1 2`
- C) `1 2 3`
- D) Fehler

---

## Antwort 10

✅ **B) `0 1 2`**

`for...in` geht durch alle **Indizes** (Positionen) eines Arrays – also `0`, `1`, `2`.

---

## Frage 11

Wie greift man auf das erste Element dieses Arrays zu?

```js
let tiere = ["Katze", "Hund", "Vogel"];
```

- A) `tiere[1]`
- B) `tiere.first()`
- C) `tiere[0]`
- D) `tiere(0)`

---

## Antwort 11

✅ **C) `tiere[0]`**

Arrays starten bei Index `0`. Das erste Element ist also immer `[0]`.

---

## Frage 12

Was hat dieses Objekt für Eigenschaften?

```js
let person = {
  name: "Max",
  alter: 13
};
```

- A) Nur `name`
- B) `name` und `alter`
- C) `"Max"` und `13`
- D) Keine

---

## Antwort 12

✅ **B) `name` und `alter`**

Ein Objekt besteht aus **Schlüssel-Wert-Paaren**. Die Schlüssel ("Eigenschaften") sind hier `name` und `alter`.

---

## Frage 13

Was gibt dieser Code aus?

```js
let person = { name: "Max", alter: 13 };
console.log(person.name);
```

- A) `person`
- B) `Max`
- C) `name`
- D) `undefined`

---

## Antwort 13

✅ **B) `Max`**

Mit dem Punkt `.` greift man auf eine Eigenschaft eines Objekts zu: `person.name` → `"Max"`.

---

## Frage 14

Was gibt dieser Code aus?

```js
let person = { name: "Max", alter: 13 };
console.log(person.alter + 2);
```

- A) `132`
- B) `alter2`
- C) `15`
- D) Fehler

---

## Antwort 14

✅ **C) `15`**

`person.alter` ist `13` (eine Zahl), `13 + 2 = 15`.

---

## Frage 15

Was gibt dieser Code aus?

```js
let x = 5;
if (x === 5) {
  console.log("Treffer!");
}
```

- A) Nichts
- B) `Treffer!`
- C) `true`
- D) `5`

---

## Antwort 15

✅ **B) `Treffer!`**

`x === 5` ist `true`, der `if`-Block wird ausgeführt. Kein `else` nötig, wenn man nur einen Fall behandeln will.

---

## Frage 16

Was wird ausgegeben?

```js
let punkte = [10, 20, 30];
let summe = 0;
for (let p of punkte) {
  summe = summe + p;
}
console.log(summe);
```

- A) `102030`
- B) `30`
- C) `60`
- D) `0`

---

## Antwort 16

✅ **C) `60`**

Die Schleife addiert alle Werte: `0 + 10 + 20 + 30 = 60`.

---

## Frage 17

Was gibt dieser Code aus?

```js
let auto = {
  marke: "VW",
  baujahr: 2010
};

for (let eigenschaft in auto) {
  console.log(eigenschaft);
}
```

- A) `VW 2010`
- B) `marke baujahr`
- C) `auto auto`
- D) Fehler

---

## Antwort 17

✅ **B) `marke baujahr`**

`for...in` bei einem Objekt gibt die **Schlüssel** (Eigenschaftsnamen) aus – nicht die Werte!

---

## Frage 18

Was gibt dieser Code aus?

```js
function sagHallo() {
  console.log("Hallo!");
}

sagHallo();
```

- A) Nichts
- B) `sagHallo`
- C) `Hallo!`
- D) Fehler

---

## Antwort 18

✅ **C) `Hallo!`**

Die Funktion wird mit `sagHallo()` aufgerufen – erst dann wird der Code darin ausgeführt.

---

## Frage 19

Was gibt dieser Code aus?

```js
function addiere(a, b) {
  return a + b;
}

console.log(addiere(3, 4));
```

- A) `a + b`
- B) `addiere`
- C) `34`
- D) `7`

---

## Antwort 19

✅ **D) `7`**

`a` und `b` sind beide Zahlen, also werden sie addiert. `return` gibt das Ergebnis zurück, `console.log` zeigt es an.

---

## Frage 20

Was gibt dieser Code aus?

```js
function begruesse(name) {
  return "Hallo " + name + "!";
}

alert(begruesse("Lisa"));
```

- A) `name`
- B) `Hallo name!`
- C) `Hallo Lisa!`
- D) Nichts

---

## Antwort 20

✅ **C) `Hallo Lisa!`**

`"Lisa"` wird als Argument übergeben, im Funktionsrumpf steht `name` dann für `"Lisa"`.

---

## Frage 21

Wie oft wird `"Hey!"` ausgegeben?

```js
function ruf() {
  console.log("Hey!");
}

ruf();
ruf();
ruf();
```

- A) Einmal
- B) Zweimal
- C) Dreimal
- D) Gar nicht

---

## Antwort 21

✅ **C) Dreimal**

Die Funktion wird drei Mal aufgerufen – jedes Mal läuft der Code darin einmal durch.

---

## Frage 22

Was gibt dieser Code aus?

```js
function verdopple(zahl) {
  return zahl * 2;
}

let ergebnis = verdopple(5);
console.log(ergebnis);
```

- A) `zahl * 2`
- B) `5`
- C) `52`
- D) `10`

---

## Antwort 22

✅ **D) `10`**

`verdopple(5)` gibt `5 * 2 = 10` zurück. Das wird in `ergebnis` gespeichert und ausgegeben.

---

## 🎉 Quiz geschafft!

Gut gemacht – das waren JS-Grundlagen und Funktionen!
