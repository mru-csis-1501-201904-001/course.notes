# COMP1501-001 Pseudocode Cheat Sheet

## Displaying something

```text
display [whatever]
```

### Notes

- displays [whatever] to some output device

### Examples

- display "That's correct!"
- display thisVariable

---

## Assigning a value to a variable

```text
[variable name] := [some value]
```

### Notes

- puts [some value] into a the variable [variable name]
- [variable name] should be descriptive; I like them in camelCase

### Examples

- myName := "Mr. Tibbs"
- numberOfDaysUntilMidsommar := 132

---

## Getting data from somewhere

```text
[variable name] := get [something]
```

### Notes

- gets the input [something] from somewhere (we typically don't care from where)

### Examples

- numParkingSpots := get number of parking spots
- userName := get user's name

---

## Finding the length of text

```text
[text variable].length()
```

### Notes

- returns the number (could be zero!) of characters in the text variable

### Examples

- if `myName` is `"Mr. Tibbs"`, then myName.length = 9
- if `userResponse` is `""`, then userResponse.length = 0

---

## Grabbing part of some text

```text
[text variable][first character index, last character index)

OR

[text variable].substring(first character index, last character index)
```

### Notes

- returns all characters from first to last index; exclusive on the right
- remember that if you subtract last index - first index, it tells you how many characters are in the result

### Examples

- if `magicPhrase` is `"gradoo"`, then magicPhrase[1,4) = magicPhrase.substring(1, 4) = "rad"
- if `exclamation` is `"Blimey!"`, then exclamation[0,1) = exclamation.substring(0, 1) "B"

---

## Getting a copy of some text in ALL CAPS

```text
[text variable].toUpperCase()
```

### Notes

- does not change [text variable] - just returns a changed copy of it

### Examples

- if `greeting` is `"hi!"`, then greeting.toUpperCase() = "HI!"
- if `mixedStatment` is `"trIpPy"`, then mixedStatment.toUpperCase() = "TRIPPY"

---

## Getting a copy of some text in lower case

```text
[text variable].toLowerCase()
```

### Notes

- does not change [text variable] - just returns a changed copy of it

### Examples

- if `greeting` is `"HI!"`, then greeting.toLowerCase() = "hi!"
- if `mixedStatment` is `"trIpPy"`, then mixedStatment.toLowerCase() = "trippy"

---

## Getting the index of the FIRST occurrence of a given character in some text

```text
[text variable].indexOf(character)
```

### Notes

- if the character is NOT in [text variable], returns -1
- is case-sensitive

### Examples

- if `magicPhrase` is `"gradoo"`, then magicPhrase.indexOfFirst("o") = 4
- if `exclamation` is `"Blimey!"`, then exclamation.indexOfFirst("b") = -1

---

## Getting the index of the LAST occurrence of a given character in some text

```text
[text variable].lastIndexOf(character)
```

### Notes

- if the character is NOT in [text variable], returns -1
- is case-sensitive

### Examples

- if `magicPhrase` is `"gradoo"`, then magicPhrase.lastIndexOf("o") = 5
- if `exclamation` is `"Blimey!"`, then exclamation.lastIndexOf("Y") = -1

---

## Replacing something in text with something else

```text
[text variable].replaceAll(thing to replace, thing to replace with)
```

### Notes

- if [thing to replace] isn't there, nothing happens
- original text isn't changed - you get a COPY back with the changes made
- is case-sensitive

### Examples

- "foo".replaceAll("o", "x") returns "fxx"
- "Hi there!".replaceAll("h", "oo") returns "Hi tooere!"

---

## Math operations

```text
any math operators you can type on the keyboard are allowed
```

### Notes

- use brackets to remove any confusion about order of operation
  - for example, if you write something like `foo + bar / baz * qux` without brackets, people are gonna hate you. And nobody wants that.
- if dividing (/), remember if BOTH numerator and denominator are integers, we do that weird integer division thing (like 4 / 8 = 0)
- the mod (%) operator gives the reminder of an integer division (like 4 % 8 = 4)

### Examples

- twiceAsGood := litresOfIceCream \* 2
- slope := (m \* x) + b
- areaOfMyLovelyCircle := pi \* (radius ^ 2)
- eggsLeftOver := numEggs % 12;

---

## Finding the maximum of two numbers

```text
max(a, b)
```

### Notes

- assume a and b are numbers
- returns the maximum of a and b
- watch out for negative nums

### Examples

- max(2, 8) = 8
- max(-3, -1) = -1
- max(121, 121) = 121

---

## Finding the minimum of two numbers

```text
min(a, b)
```

### Notes

- assume a and b are numbers
- returns the minimum of a and b
- watch out for negative nums

### Examples

- min(2, 8) = 2
- min(-3, -1) = -3
- min(121, 121) = 121

---

## Finding the ceiling of a number

```text
ceiling(a)

OR

ceil(a)
```

### Notes

- assume a is a number
- general definition: https://www.mathsisfun.com/sets/function-floor-ceiling.html
- for negative numbers: https://math.stackexchange.com/q/344815

### Examples

- ceiling(2.0001) = 3
- ceiling(4321) = 4321
- ceiling(-2.8) = -2
- ceiling(-2.01) = -2

---

## Finding the floor of a number

```text
floor(a)
```

### Notes

- assume a is a number
- general definition: https://www.mathsisfun.com/sets/function-floor-ceiling.html
- for negative numbers: https://math.stackexchange.com/q/344815

### Examples

- floor(2.99999) = 2
- floor(4321) = 4321
- floor(-2.8) = -3
- floor(-2.01) = -3

---

## Rounding a number

```text
round(a)
```

### Notes

- assume a is a number
- works like you learned in high school
- be careful with negative nums (see examples)

### Examples

- round(2.4) = 2
- round(2.5) = 3
- round(4321) = 4321
- round(-2.8) = -3
- round(-2.5) = -2
- round(-2.4) = -2

---

## Selection

```text
if ([condition]) then
  // code to run if [condition] is true
end if

OR

if ([condition]) then
  // code to run if [condition] is true
else
  // code to run if [condition] is false
end if

OR

if ([condition 1]) then
  // code to run if [condition 1] is true
else if ([condition 2]) then
  // code to run if [condition 2] is true
else
  // code to run if none of the prior conditions are true
end if
```

### Notes

- [condition] is anything that evaluates to true or false
  - [ ] can be a simple comparison (like x <= 10)
  - [ ] can be more complex, with AND, OR, and !(not) (like height > 10 OR (name == "john" AND age != 2))

### Examples

- ```java
  if (missileCode = 123) then
    display "launching missiles"
  end if
  ```
- ```java
  if (daysInFridge > 20 AND foodColor = "green") then
    return "throw that out!"
  else
    return "should be safe..."
  end if
  ```
- ```java
  if (day = 25 AND month = "December") then
    // Santa is coming
  else if (day = 31 AND month = "October") then
    // the Great Pumpkin is coming
  else if (today.isEaster()) then
    // the Easter Bunny is coming
  else
    // your life is a joyless thing
  end if
  ```

---

## Looping

```text
do/repeat n times
  // code to run n times
end

OR

while ([condition]) do
  // code to run while [condition] is true
end

OR

do/repeat
  // code to run while [condition] is true
while ([condition])

OR

do/repeat
  // code to run until [condition] is true
until ([condition])

OR

for (i = [low] to [high]) do
  // code to run while i is <= high
  // i increases by one each time
end

OR

for each ([thing] in [collection of things]) do
  // code to run with [thing]
  // each [thing] in [collection] is provided once, in order
end
```

### Notes

- [condition] is anything that evaluates to true or false
  - [ ] can be a simple comparison (like x <= 10)
  - [ ] can be more complex, with AND, OR, and !(not) (like height > 10 OR (name == "john" AND age != 2))

### Examples

- ```text
  repeat 3 times
    display "There's no place like home."
  end
  ```

- ```text
  while (life > 0 AND gold > 0)
    playOneRound()
  end
  ```

- ```text
  repeat
    mark := get mark from file
    display mark
  while (marksLeftInFile)
  ```

- ```text
  do
    grab a handful of popcorn
    shove handful in mouth
  until (popcornIsGone)
  ```

- ```text
  for (i = 0 to word.length()) do
    letter = word.substring(i, i + 1)
    if (letter is a vowel) then
      print "that's a vowel"
    end if
  end
  ```

- ```text
  for each (letter in word) do
    if (letter is a vowel) then
      print "that's a vowel"
    end if
  end
  ```

---
