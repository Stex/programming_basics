# Einfache Datentypen

- [Einfache Datentypen](#einfache-datentypen)
  - [Booleans / Wahrheitswerte](#booleans--wahrheitswerte)
  - [Numbers / Zahlen](#numbers--zahlen)
  - [Strings / Zeichenketten](#strings--zeichenketten)

> In den folgenden Beispielen steht oft um den eigentlichen Code immer noch ein `console.log()`, dies sorgt
nur dafür, dass das Ergebnis des Codes in den runden Klammern in der Konsole ausgegeben wird,
wenn diese Datei hier mit `lit-node docs/001-einfache-datentypen.md` ausgeführt wird.

Wenn wir über bestimmte Dinge sprechen ordnen wir sie automatisch in Kategorien ein. So ist "2"
bspw. eine Zahl, "Apfel" ist ein Wort (und eine Frucht), "Peter, Paul und Mary" ist eine Aufzählung
von Personen.

Auch, wenn es vielleicht etwas holprig erscheinen mag, lässt sich dieses Konzept auch darauf
übertragen, wie Programmiersprachen funktionieren. Diese bieten uns von Haus aus verschiedene Kategorien von Dingen an, mit denen wir arbeiten können, die sogenannten Datentypen.

Die folgende kleine Auswahl wird uns in der ersten Zeit in Javascript häufig begegnen:

## Booleans / Wahrheitswerte

Es gibt nur zwei mögliche Wahrheitswerte:

* `true` (also wahr) und
* `false` (also falsch)

Wie auch unserem normalen Sprachgebrauch kann etwas nur entweder wahr oder falsch sein, niemals beides gleichzeitig. Zusätzlich gilt: Wenn etwas nicht wahr ist, ist es falsch. Und wenn etwas nicht falsch ist, ist es wahr (hier ist die Programmierung ziemlich strikt, sowas wie "ein bisschen wahr" gibt es nicht).

Booleans werden in der Programmierung oft als Bedingung verwendet, also z.B., um ein Programm
bestimmte Dinge nur unter bestimmten Bedingungen tun zu lassen.  
Die folgenden Beispiele sind jeweils einmal in natürlicher Sprache und einmal mit Wahrheitswerten formuliert:

> Wenn der Nutzer ein Affe ist, gib eine 🍌 auf dem Bildschirm aus  
> Wenn es wahr ist, dass der Nutzer ein Affe ist, gib eine 🍌 auf dem Bildschirm aus

```
WENN(nutzerIstAffe == true) DANN 🍌
```

> Solange der Nutzer noch nicht aufgestanden ist, lasse den Wecker weiterklingeln  
> Solange es falsch ist, dass der Nutzer aufgestanden ist, lasse den Wecker weiterklingeln

```
SOLANGE(nutzerIstAufgestanden == false) LASSE WECKER KLINGELN
```

In dem obigen Pseudocode wurde `==` verwendet. Dies ist ein Operator, mit dem man zwei Dinge
vergleichen kann. Der `==`-Operator gibt immer einen Boolean zurück, nämlich

* `true`, wenn die beiden Werte gleich sind
* `false`, wenn sie nicht gleich sind

Wie oben schon beschrieben wird `true` niemals gleich `false` sein, das lässt sich mit `==` so testen:

```js
console.log(true == true)    // => true
console.log(false == false)  // => true
console.log(false == true)   // => false
console.log(true == false)   // => false
```

Zudem gibt es als Gegenstück zum Gleichheitsoperator `==` auch den Ungleichheitsoperator `!=`.
Dieser gibt `true` zurück, wenn zwei Werte nicht gleich sind und `false`, wenn sie gleich sind:

```js
console.log(true != true)    // => false
console.log(false != false)  // => false
console.log(false != true)   // => true
console.log(true != false)   // => true
```

Wenn man sich `==` und `!=` anschaut, kann man diese Operatoren als "gleich" und "nicht gleich" lesen.  
Das Ausrufezeichen entspricht hier dem Wort "nicht" und kann auch tatsächlich so in Javascript verwendet werden:

```js
console.log(!true)  // => false
console.log(!false) // => true
```

Damit ließe sich ein "ungleich" auch wie folgt ausdrücken, die beiden Zeilen tun das gleiche:

```js
console.log(true != true)    // => true
console.log(!(true == true)) // => false
```

## Numbers / Zahlen

Unter Zahlen fallen in Javascript sowohl Ganzzahlen (1, 2, 3, ...) als auch Fließkommazahlen (1.5, 3.1315).

Bei der Arbeit mit Zahlen können wir viele aus der Mathematik bekannte Operatoren verwenden:

```js
console.log(1 + 1)  // => 2
console.log(2 - 1)  // => 1
console.log(2 * 2)  // => 4
console.log(8 / 2)  // => 4
```

Zusätzlich gibt es nun auch noch weitere Operatoren, die wie schon `==` und `!=` einen Boolean-Wert
zurückgeben, nämlich die Vergleichsoperatoren:

* `==` (Ein Wert ist gleich dem anderen)
* `!=` (Ein Wert ist ungleich dem anderen)
* `>`  (Ein Wert ist größer als der andere)
* `<`  (Ein Wert ist kleiner als der andere)
* `>=` (Ein Wert ist größer oder gleich dem anderen)
* `<=` (Ein Wert ist kleiner oder gleich dem anderen)

```js
console.log(5 > 2)  // => true
console.log(9 <= 9) // => true
console.log(2 >= 3) // => false
```

## Strings / Zeichenketten

Ein String ist eine Liste von Zeichen, die von Anführungszeichen (`"`) oder Hochkommata (`'`, wichtig:
das ist kein Akzent!) eingeschlossen werden.

Beispiele hier sind:

```js
"Hallo Welt"
'Javascript'
```

Aber auch

```js
"¯\_(ツ)_/¯"
"🙉 🙈 🙊"
```

Ein String bringt direkt einige Methoden (dazu später mehr) mit, die es einfach machen, mit ihnen zu arbeiten. Die folgenden Methoden sind natürlich nur eine kleine Auswahl.

Wenn ich im folgenden "#" vor ein Wort schreibe, meine ich damit einen Methodennamen.

```js
// #length gibt die Anzahl Zeichen in einem String als Zahl zurück
console.log("abcde".length)  // => 5

// #+ "klebt" die beiden Strings zusammen und gibt den neuen String zurück
console.log("Hallo " + "Welt")  // => "Hallo Welt"

// #includes Prüft, ob ein String einen anderen enthält und gibt ein Boolean zurück
console.log("affenhaus".includes("haus"))  // => true
console.log("affenhaus".includes("baum"))  // => false
```