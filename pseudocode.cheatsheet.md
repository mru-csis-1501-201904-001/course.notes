# COMP1501-001 Pseudocode Cheat Sheet

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
```

### Notes

- returns all characters from first to last index; exclusive on the right

### Examples

- if `magicPhrase` is `"gradoo"`, then magicPhrase[1,4) = "rad"
- if `exclamation` is `"Blimey!"`, then exclamation[0,1) = "B"

---

## Math operations

```text
any math operators you can type on the keyboard are allowed
```

### Notes

- use brackets to remove any confusion about order of operation
  - for example, if you write something like `foo + bar / baz * qux` without brackets, people are gonna hate you. And nobody wants that.

### Examples

- twiceAsGood := litresOfIceCream \* 2
- slope := (m \* x) + b
- areaOfMyLovelyCircle := pi \* (radius ^ 2)

---

## Getting the index of the FIRST occurrence of a given character in some text

```text
[text variable].indexOfFirst(character)
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
[text variable].indexOfLast(character)
```

### Notes

- if the character is NOT in [text variable], returns -1
- is case-sensitive

### Examples

- if `magicPhrase` is `"gradoo"`, then magicPhrase.indexOfLast("o") = 5
- if `exclamation` is `"Blimey!"`, then exclamation.indexOfFirst("Y") = -1

---
