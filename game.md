# DOM Manipulation

Von HTML zu JavaScript

---

## Was haben wir bisher?

```javascript
for (let r of [1, 2, 3, 4, 5]) {
    for (let c of [1, 2, 3, 4, 5]) {
        document.writeln(`<div class="cell"></div>`);
    }
}
```

Das funktioniert, aber...

---

## Problem mit `document.writeln()`

- Schreibt HTML als Text
- Kann nur beim Laden der Seite verwendet werden
- Schwer zu ändern oder zu erweitern
- Für Spiele brauchen wir **dynamisches** HTML!

---

## Die bessere Lösung

**JavaScript kann HTML-Elemente erstellen!**

Das nennt man **DOM Manipulation**

---

## Was ist das DOM?

**DOM = Document Object Model**

Das DOM ist der "Baum" aller HTML-Elemente:

```
html
├── head
│   └── title
└── body
    ├── div.board
    │   ├── div.cell
    │   └── div.cell
    └── script
```

---

## Elemente mit JS erstellen

### Schritt 1: Element erstellen

```javascript
const cell = document.createElement('div');
```

Erstellt ein neues `<div>` Element (noch unsichtbar!)

---

## Elemente mit JS erstellen

### Schritt 2: Klasse hinzufügen

```javascript
const cell = document.createElement('div');
cell.className = 'cell';
```

Gibt dem Element die CSS-Klasse `cell`

---

## Elemente mit JS erstellen

### Schritt 3: Element einfügen

```javascript
const cell = document.createElement('div');
cell.className = 'cell';

const board = document.querySelector('.board');
board.appendChild(cell);
```

**Jetzt wird es sichtbar!**

---

## Der komplette Code

```javascript
const board = document.querySelector('.board');

const cell = document.createElement('div');
cell.className = 'cell';
board.appendChild(cell);
```

Erstellt **eine** Zelle (wird automatisch ins Grid eingefügt)

---

## Übung 1

Erstelle **drei** Zellen:

**Tipp:** Kopiere den Code 3x!

---

## Lösung Übung 1

```javascript
const board = document.querySelector('.board');

// Zelle 1
const cell1 = document.createElement('div');
cell1.className = 'cell';
board.appendChild(cell1);

// Zelle 2
const cell2 = document.createElement('div');
cell2.className = 'cell';
board.appendChild(cell2);

// Zelle 3
const cell3 = document.createElement('div');
cell3.className = 'cell';
board.appendChild(cell3);
```

---

## Das ist viel Code...

**Gibt es nicht eine bessere Lösung?**

Ja! Schleifen!

---

## Eine Zeile mit Schleifen

```javascript
const board = document.querySelector('.board');

for (let c = 1; c <= 5; c++) {
    const cell = document.createElement('div');
    cell.className = 'cell';
    board.appendChild(cell);
}
```

Erstellt **5 Zellen** in einer Zeile

---

## Wie funktioniert das?

```javascript
for (let c = 1; c <= 5; c++) {
    const cell = document.createElement('div');
    cell.className = 'cell';
    board.appendChild(cell);
}
```

**c=1:** Eine Zelle wird erstellt
**c=2:** Eine Zelle wird erstellt
**c=3:** Eine Zelle wird erstellt
**c=4:** Eine Zelle wird erstellt
**c=5:** Eine Zelle wird erstellt

→ **5 Zellen insgesamt**

---

## Übung 2

Ändere den Code so, dass **10 Zellen** in einer Reihe entstehen.

**Tipp:** Was musst du ändern?

---

## Lösung Übung 2

```javascript
const board = document.querySelector('.board');

for (let c = 1; c <= 10; c++) {  // 10 statt 5
    const cell = document.createElement('div');
    cell.className = 'cell';
    board.appendChild(cell);
}
```

**Vergiss nicht:** CSS Variable `--cols` auch auf 10 setzen!

---

## Jetzt wird's spannend

**Wie machen wir mehrere Zeilen?**

Wir brauchen eine **zweite Schleife drumherum**!

---

## Eine zweite Schleife

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 5; r++) {
    // Hier kommt die Spalten-Schleife hin
}
```

Diese Schleife macht **5 Zeilen**

---

## Beide Schleifen zusammen

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 5; r++) {
    for (let c = 1; c <= 5; c++) {
        const cell = document.createElement('div');
        cell.className = 'cell';
        board.appendChild(cell);
    }
}
```

**Äußere Schleife:** 5 Zeilen
**Innere Schleife:** 5 Spalten pro Zeile
**= 25 Zellen insgesamt**

---

## Wie funktioniert das?

```javascript
for (let r = 1; r <= 5; r++) {
    for (let c = 1; c <= 5; c++) {
        // Zelle erstellen
    }
}
```

**r=1:** Innere Schleife läuft 5x → Zeile 1 mit 5 Zellen
**r=2:** Innere Schleife läuft 5x → Zeile 2 mit 5 Zellen
**r=3:** Innere Schleife läuft 5x → Zeile 3 mit 5 Zellen
**r=4:** Innere Schleife läuft 5x → Zeile 4 mit 5 Zellen
**r=5:** Innere Schleife läuft 5x → Zeile 5 mit 5 Zellen

---

## Visualisierung

```
r=1: [Zelle] [Zelle] [Zelle] [Zelle] [Zelle]
r=2: [Zelle] [Zelle] [Zelle] [Zelle] [Zelle]
r=3: [Zelle] [Zelle] [Zelle] [Zelle] [Zelle]
r=4: [Zelle] [Zelle] [Zelle] [Zelle] [Zelle]
r=5: [Zelle] [Zelle] [Zelle] [Zelle] [Zelle]
```

5 Zeilen × 5 Spalten = **25 Zellen**

---

## Der komplette Code

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 5; r++) {
    for (let c = 1; c <= 5; c++) {
        const cell = document.createElement('div');
        cell.className = 'cell';
        board.appendChild(cell);
    }
}
```

**Das CSS Grid macht automatisch die richtige Anordnung!**

---

## Übung 3

Erstelle ein **10×10 Grid**

**Denke daran:**
1. Beide Schleifen auf 10 ändern
2. CSS Variablen `--cols` und `--rows` auf 10 setzen

---

## Lösung Übung 3

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 10; r++) {
    for (let c = 1; c <= 10; c++) {
        const cell = document.createElement('div');
        cell.className = 'cell';
        board.appendChild(cell);
    }
}
```

**CSS:**
```css
:root {
    --cols: 10;
    --rows: 10;
}
```

---

## Jetzt wird's cool! 🎮

**Verschiedene Zelltypen:**

- `cell` = normale Zelle
- `wall` = Wand
- `hero` = Spieler
- `door` = Tür
- `monster-1` = Monster

---

## Bedingte Klassen

```javascript
if (r === 1 || r === 5 || c === 1 || c === 5) {
    cell.className = 'cell wall';
} else {
    cell.className = 'cell';
}
```

**Übersetzung:**
Wenn am Rand (erste oder letzte Zeile/Spalte) → Wand
Sonst → normale Zelle

---

## Komplettes Grid mit Wänden

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 5; r++) {
    for (let c = 1; c <= 5; c++) {
        const cell = document.createElement('div');

        if (r === 1 || r === 5 || c === 1 || c === 5) {
            cell.className = 'cell wall';
        } else {
            cell.className = 'cell';
        }

        board.appendChild(cell);
    }
}
```

**Jetzt haben wir Wände am Rand!**

---

## Mehrere Bedingungen

```javascript
if (r === 1 || r === 5 || c === 1 || c === 5) {
    cell.className = 'cell wall';
} else if (r === 3 && c === 3) {
    cell.className = 'cell hero';
} else if (r === 2 && c === 4) {
    cell.className = 'cell door';
} else {
    cell.className = 'cell';
}
```

**Wir können verschiedene Positionen verschiedene Klassen geben!**

---

## Übung 4

Erstelle ein 10×10 Grid mit:

- Wände am Rand (erste und letzte Zeile/Spalte)
- Hero in der Mitte (Zeile 5, Spalte 5)
- Eine Tür oben in der Mitte (Zeile 1, Spalte 5)
- Alles andere normale Zellen

---

## Lösung Übung 4

```javascript
const board = document.querySelector('.board');

for (let r = 1; r <= 10; r++) {
    for (let c = 1; c <= 10; c++) {
        const cell = document.createElement('div');

        if (r === 1 || r === 10 || c === 1 || c === 10) {
            cell.className = 'cell wall';
        } else if (r === 5 && c === 5) {
            cell.className = 'cell hero';
        } else if (r === 1 && c === 5) {
            cell.className = 'cell door';
        } else {
            cell.className = 'cell';
        }

        board.appendChild(cell);
    }
}
```

---

## Zusammenfassung

**Wir haben gelernt:**

1. ✅ `document.createElement()` - Elemente erstellen
2. ✅ `element.className` - Klassen setzen
3. ✅ `element.appendChild()` - Elemente einfügen
4. ✅ Erst eine Schleife für eine Zeile
5. ✅ Dann eine zweite Schleife drumherum für mehrere Zeilen
6. ✅ Bedingte Klassen mit `if/else`

**CSS Grid macht die Anordnung automatisch!**

---

## Nächste Schritte

Jetzt können wir:

- Das Board dynamisch aufbauen
- Den Hero bewegen (mit Tasten)
- Monster hinzufügen
- Kollisionen prüfen
- Ein echtes Spiel bauen! 🎮

---

## Hausaufgabe (optional)

Experimentiere mit:

- Größere Grids (15×15, 20×20)
- Verschiedene Muster für Wände
- Mehrere Monster an verschiedenen Positionen
- Zufällige Positionen mit `Math.random()`

---

## Gut gemacht! 🎉

Ihr seid jetzt bereit für Game Development!