# Weitere Operationen
// Ganzzahlige Division:    Division, aber immer abrunden

Int(a):                     Immer zur Null hin runden

% Modulo:                   Rest von der letzten ganzzahligen Division (a%b --> für b > a : a --> bspw. für a = 5 und b = 4 : 1)

# Funktionen
```
def Funktion(parameter):
  Operationen
  return Variable
```
# Weitere Module
## Random
```
random()                             # Random float:  0.0 <= x < 1.0
0.37444887175646646

uniform(2.5, 10.0)                   # Random float:  2.5 <= x <= 10.0
3.1800146073117523

expovariate(1 / 5)                   # Interval between arrivals averaging 5 seconds
5.148957571865031

randrange(10)                        # Integer from 0 to 9 inclusive
7

randrange(0, 101, 2)                 # Even integer from 0 to 100 inclusive
26

choice(['win', 'lose', 'draw'])      # Single random element from a sequence
'draw'

deck = 'ace two three four'.split()
shuffle(deck)                        # Shuffle a list
deck
['four', 'two', 'ace', 'three']

sample([10, 20, 30, 40, 50], k=4)    # Four samples without replacement
[40, 10, 50, 30]
```

## Turtle
```
forward() | fd()
backward() | bk() | back()
right() | rt()
left() | lt()
goto() | setpos() | setposition()
setx()
sety()
setheading() | seth()
home()
circle()
dot()
stamp()
clearstamp()
clearstamps()
undo()
speed()
pendown() | pd() | down()
penup() | pu() | up()
pensize() | width()
pen()
isdown()
```

# if-else Anweisungen
```
def is_number(a) :
    if type(a) == int:
        return True
    elif type(a) == float:
        return True
    else: # a ist weder eine int-Zahl noch eine float-Zahl
        return False
    
print(is_number(7.3))  # True
print(is_number("Hallo"))  # False
```

# while Anweisung
Eine while-Anweisung wird verwendet, um eine Folge von Anweisungen zu wiederholen, wenn eine bestimmte Bedingung erfüllt ist
```
i = 1
while i < 10:
    print("in Schleife")
    i = i + 1
```
Die Schleife wird mehrmals (9 mal) durchlaufen. Die Abfrage (i<10) wird einmal mehr, d.h. 10 mal durchlaufen.

# for Anweisung
Eine for-Anweisung ist eine Wiederholungsanweisung, die man für eine bekannte Folge von Werten durchführen möchte.
```
for <Variable> in <Sequenz> :
   <Anweisungen>
```
<Sequenz> entspricht einer Folge von Werten

<Variable> nimmt nacheinander die Werte der Folge an

<Anweisungen> werden für jeden der Werte der Folge einmal ausgeführt

# range Funktion
range(m) - erzeugt Sequenz der ganzen Zahlen von 0 bis m-1 (jeweils inklusive)

range(n,m) - erzeugt Sequenz der ganzen Zahlen von n bis m-1 (jeweils inklusive)

range(n,m,k) - erzeugt Sequenz der ganzen Zahlen von n (inklusive) bis echt kleiner m bei positiver Schrittweite k und von n (inklusive) bis echt größer m bei negativer Schrittweite k

# find Funktion
```
text = "eGuten Morgen"
index1 = text.find("en")  # 4
print("index2:",text.find("en", index1 + 1))  # 11
```

# split Funktion
```
text = "Guten Morgen"
datum = "19.07.2023"
a = text.split()  # ['Guten','Morgen']
b = datum.split(".")  # ['19','07','2023']
```

# Sprunganweisungen
**return** beendet eine Funktion

**break** beendet eine Wiederholungsanweisung (while oder for)

**continue** beendet die aktuelle Ausführung einer Wiederholungsanweisun

# Liste
```
liste = [1,2,3,4,5]
liste2 = [6,7,8]
print(liste1 + liste2)  # [1,2,3,4,5,6,7,8]
print(2 in liste)  # True
print(6 in liste)  # False
liste < liste2  # True --> Vergleich wird zeilenweise durchgeführt
```

# Tupel
```
tupel = ("Berlin", "Leipzig", "Hannover")
tupel2 = (1, 2, 3)
tupel1 + tupel2 = ("Berlin", "Leipzig", "Hannover", 1, 2, 3)
In Listen und Tupel können auch Daten unterschiedlichen Tyos sein.
```

# Slice
Ein Teilbereich einer Sequenz nennt man einen Slice und kann diesen über den Operator [ ] bestimmen. Im folgenden sind i und j ganze Zahlen, die für einen Index stehen:

[i] : Ergebnis ist der Wert der Sequenz an dem Index

[i:j] : Ergebnis ist die Teilsequenz ab inklusive Index i bis exklusive Index j

[i:] : Ergebnis ist die Teilsequenz ab inklusive Index i bis zum Ende der Sequenz

[:j] : ergebnis ist die Teilsequenz ab dem Anfang bis exklusive Index j

# Ändern von Listen
```
insert(i, v) – fügt den Wert v an Index i ein; nachfolgende Elemente werden um eine Position verschoben
remove(v) – entfernt den Wert v aus der Liste, falls vorhanden!
append(v) – hängt den Wert v an das Ende der Liste
reverse() – kehrt die Reihenfolge der Werte in der Liste um
sort() – sortiert die Werte in der Liste
```

# Beispiel: Umkehren einer Liste ohne python eigene Funktionen
```
for i in range(len(farben)-1,-1,-1):
    print(farben[i])
```
# Dictionaries
* Schlüssel-Wert-Paare
```
students = {111 : "Max Mustermann", 
            112 : "Erika Musterfrau",
            113 : "Otto Normalverbraucher", 
            114 : "Lieschen Müller"}
print(students[111])  # Max Mustermann
print(students.get(111))  # Max Mustermann
students[111] = "Emty"  # Überschreiben des Eintrags 111
````
Mittels der Funktionen keys() und values() erhält man eine Sicht auf die Schlüssel bzw. Werte eines Dictionarys. Sicht heißt in diesem Fall, dass man eine Referenz auf die entsprechenden Schlüssel/Werte erhält und keine Kopie.
````
print(students.keys())  # dict_keys([111111, 111112, 111113, 111114])
print(students.values())  # dict_values(['Max Mustermann', 'Erika Musterfrau', 'Otto Normalverbraucher', 'Lieschen Müller'])
```

