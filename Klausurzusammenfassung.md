# Weitere Operationen
// Ganzzahlige Division:    Division, aber immer abrunden
Int(a):                     Immer zur Null hin runden
% Modulo:                   Rest von der letzten ganzzahligen Division (a%b  für b > a : a  bspw. für a = 5 und b = 4 : 1)

# Funktionen
def Funktion(parameter):
  Operationen
	return Variable

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
    
print(is_number(7.3))
print(is_number("Hallo"))
```
