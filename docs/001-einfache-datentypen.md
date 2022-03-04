# Einfache Datentypen

Wenn wir über bestimmte Dinge sprechen ordnen wir sie automatisch in Kategorien ein. So ist "2"
bspw. eine Zahl, "Apfel" ist ein Wort (und eine Frucht), "Peter, Paul und Mary" ist eine Aufzählung
von Personen.

Auch, wenn es vielleicht etwas holprig erscheinen mag, lässt sich dieses Konzept auch darauf
übertragen, wie Programmiersprachen funktionieren.

Diese bieten uns von Haus aus verschiedene Kategorien von Dingen an, mit denen wir arbeiten können,
die sogenannten Datentypen.

Die folgende kleine Auswahl wird uns in der ersten Zeit in Javascript häufig begegnen:

## String / Zeichenketten

Ein String ist eine Liste von Zeichen, die von Anführungszeichen (`"`) oder Hochkommata (`'`, wichtig:
das ist kein Akzent!) eingeschlossen werden.

Beispiele hier sind:

```javascript
"Hallo Welt"
'Javascript'
```

Aber auch

```javascript
"¯\_(ツ)_/¯"
"🙉 🙈 🙊"
```

Ein String bringt direkt einige Methoden (dazu später mehr) mit, die es einfach machen, mit ihnen zu arbeiten.

In den folgenden Beispielen steht um den eigentlichen Code immer noch ein `console.log()`, dies sorgt
nur dafür, dass das Ergebnis des Codes in den runden Klammern in der Konsole ausgegeben wird,
wenn diese Datei hier mit `lit-node` ausgeführt wird.

```javascript
// "string".length gibt die Anzahl Zeichen in einem String zurück
console.log("abcde".length)

// "string 1" + "string 2" klebt die beiden Strings zusammen und gibt den neuen String zurück
console.log("Hallo " + "Welt")
```