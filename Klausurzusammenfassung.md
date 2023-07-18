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
```
Mittels der Funktionen keys() und values() erhält man eine Sicht auf die Schlüssel bzw. Werte eines Dictionarys. Sicht heißt in diesem Fall, dass man eine Referenz auf die entsprechenden Schlüssel/Werte erhält und keine Kopie.
```
print(students.keys())  # dict_keys([111111, 111112, 111113, 111114])
print(students.values())  # dict_values(['Max Mustermann', 'Erika Musterfrau', 'Otto Normalverbraucher', 'Lieschen Müller'])
```

# Numpy
Erstellung von Arrays [1 2 3]
```
arange(start, stop, step, dtype)
start – Startwert (inklusive)
stop – Endwert (exklusive)
step – Schrittweite
dtype – Datentyp der erzeugten Werte
```
## linspace
```
linspace(start, stop, num=50, endpoint=True, retstep=False)
start , stop – erster , letzter Wert
num – Anzahl der Werte
endpoint – wenn True, dann inklusive Wert stop, sonst exklusiv
retstep – wenn True, wird neben Array die Schrittweite zurückgeliefert
```
Ausgabe nur von float-Werten, da keine Schrittweite, sondern gewünschte Anzahl von Werten. Bsp.: [0. 1. 2. 3. 4. 5.]
Konvertierung von Listen in Array, wenn Listeninhalte gleich lang sind
```
a = np.array([[1,2], [3,4], [5,6]])  # [[1 2] [3 4] [5 6]]
np.array([[1,2], [3,4], [5]])  # error
a[1,1]  # 4
```

## ndim & shape
ndim: Dimension des Arrays --> für [[1,2] [3,4] [5,6]]  ndim = 2 --> für [[[1,2] [3,4] [5,6]]]  ndim = 3
shape: Länge des Arrays bestimmen --> für [[1,2] [3,4] [5,6]]  shape = (3,2)

## Spezielle Arrays
```
np.ones((7))  # [1. 1. 1. 1. 1. 1. 1.]
np.zeros((5), int)  # [0 0 0 0 0]
np.ones((3), bool)  # [True True True]
np.zeros((4,4), int)
[[0 0 0 0]
 [0 0 0 0]
 [0 0 0 0]
 [0 0 0 0]]
```
## Rechnen mit Arrays
Selber Shape und Type benötigt, sonst Fehler
```
a = np.array([1,2,3])  # [1 2 3]
b = a * 3  # [3 6 9]
b = a + 1  # [2 3 4]

```

# Matplot
```
import matplotlib.pyplot as plt

plt.plot([-1, -6.3, 16, 23, 15, 100])  # Wenn nur eine Wertereihe gegeben, werden diese für y genommen, x Schrittweite ist 1
plt.show()
```

![image](https://github.com/s92854/Informatik/assets/134683810/4b40344b-9b27-4858-96ad-a19c53c140ae)

### Bedeutungen
'o' : Punkte darstellen
'--' : zu verbindende Linie gestrichelt
'-' : durchgezogene Linie
'r' für red, 'b' für blue, 'g' für green, usw.

```
days = list(range(1,6))
TempCelsiusMax = [24.8, 28.9, 31.3, 23.7, 26.9]
TempCelsiusMin = [19.6, 24.1, 24.7, 18.3, 17.5]
plt.plot(days, TempCelsiusMax,
         days, TempCelsiusMin)
plt.xlabel('Tag')
plt.ylabel('Temperatur (C)')
```

![image](https://github.com/s92854/Informatik/assets/134683810/76435d89-20fe-422a-81a7-da328fca45db)

```
import numpy as np

x = np.linspace(0, 2 * np.pi, 50) # generiert Array mit 50 Werte im Bereich 0 .. 2*PI
y = np.sin(x)  # generiert Array mit Werten sin(x) für alle Werte aus x
#print(y)
plt.plot(x,y)
plt.show()
```

![image](https://github.com/s92854/Informatik/assets/134683810/08d8fbe6-0cfe-491f-bd06-a1554e2d9a4c)

Werte übereinander plotten, Legende, Datei speichern
```
fig = plt.figure(figsize=(15,8),dpi=100)
werte1 = [7, 11, 20, 8, 23, -8, 19, 9, 11, 4, -3, 5]
werte2 = [3, 31, 7, 10, 14, -2, 16, 1, -5, -3, 3, 7]
plt.plot(werte1, label='Werte1')
plt.plot(werte2, label='Werte2')
plt.legend(loc = 'upper right')
fig.savefig('beispielplot')
```

![image](https://github.com/s92854/Informatik/assets/134683810/883b3c5d-667c-4fbd-85cb-5828a70ec36a)

# Dateien
```
fobj = open("points.txt","r")

r – für „read“, w – für „write“, d.h. schreiben; dabei wird eine vorhandene Datei zuerst gelöscht
a - für „append“; es wird am Ende einer ggf. vorhandenen Datei geschrieben
b – zum Öffnen im Binärmodus; hier handelt es sich um eine zusätzliche Angabe zu den vorigen Modi

fobj.close()

readline – zum Lesen einer einzelnen Zeile in einen String          # lines = fobj.readline()  # Zeile 1 der geöffneten Datei
readlines – zum Lesen aller Zeilen in eine Liste von Strings        # lines = fobj.readlines()  # ['Zeile 1\n','Zeile 2\n','Letzte Zeile']
read – zum Lesen des Inhalts der gesamten Datei in einen String     # lines = fobj.readline()  #  Zeile 1
                                                                                                  Zeile 2
                                                                                                  Letzte Zeile
```
```
lines = fobj.readlines()   # lines Liste mit allen Zeilen einer Datei

points = []         # In points Liste Tupeln; jedes Tupel entspricht einem Punkt
for line in lines:     # iterieren durch alle Texte/Zeilen der Liste
    point = line.split(",")  # Zerlegen des Textes einer Zeile
    name = point[0]
    x = int(point[1])
    y = int(point[2])
    points.append((name,x,y))  # Tupel an das Ende der Liste anfügen
```
Schreiben:
```
def anonlist(filename):
    # Erstellen der Datei und Hinzufügen der Endung _anonym
    anonym_filename = filename.split('.')[0] + '_anonym.txt'

    with open(filename, 'r') as file:
            # Anfordern des Schreibzugriffs
            with open(anonym_filename, 'w') as anonym_file:
                # Erstellung des Counters
                counter = 1
                for line in file:
                    # Splitten der Eigenschaften (Nachname, Vorname, Matrikelnummer und Note)
                    parts = line.strip().split(', ')
                    # Die Anzahl der Eigenschaften muss 4 betragen, damit die Noten in die anonyme Datei übertragen werden
                    if len(parts) == 4:
                        # Zugriff auf Position 3 (Note)
                        note = parts[3]
                        # Schreiben der Nummer und Note in die Textdatei und Erhöhung des Counters um 1
                        anonym_file.write("{}: {}\n".format(counter,note))
                        counter += 1
    return anonym_filename
```

# Ausnahmebehandlungen
**ValueError** : tritt auf, wenn eine Zeichenkette versucht wird als ein Zahlenwert zu interpretieren, die Zeichenkette aber nicht dem entsprechenden Typ entspricht

**ZeroDivisionError** : tritt bei Division durch 0 auf

**IOError** : tritt beim Zugriff auf Dateien auf

**IndexError** : tritt auf, wenn bei einer Sequenz ein falscher Index verwendet wird

```
try :
except ValueError :
    print("Falsches Zahlenformat bei Eingabe!")
except ZeroDivisionError :
    print("Division durch 0 ist nicht erlaubt!")
except :
    print("unbekannter Fehler")
```

# Klassen
