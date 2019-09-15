# MRU Username Generator Challenge

## The problem

We have student records in this format:

`"[last name],[first name],[id number]"`

We want to create a method that will generate an MRU username from a given record. To do so, you take the first initial of the first name, the first 4 letters of the last name, and the last 3 digits of the id and concatenate them all together. Everything has to be in lowercase.

For example, if we are given the record `"Bond,James, 123456007"`, then we want the generated username to be `"jbond007"`.

## Generate examples to understand the problem

You should think of some example inputs and their corresponding outputs to see if you really understand what's being asked. Making examples will greatly help catching situations that need clarification.

| Input                  | Expected Output |
| ---------------------- | --------------- |
| "Bond,James,123456007" | "jbond007"      |
| "BOND,Jill,00007"      | "jbond007"      |
| "d,e,12345209"         | "ed209"         |

| Unacceptable Inputs |
| ------------------- |
| ",James,123456007"  |
| "b,,1234567"        |
| "Macneil,DJ,12"     |

## Assumptions/Restrictions

- the last name and first name will each have >= 1 character
- the id number will have at >= 3 characters

## A natural language algorithm for a method that solves the problem

```text
get the student record

grab the first name by getting the text between the 2 commas

grab the first initial of that first name

grab the last name by getting the text up to (but not including) the first comma

grab the first 4 letters of that last name

grab the id by getting the text after the last comma

grab the last 3 digits of that id

return the first initial(lowercased) + first 4 of last (lowercased) + last 3 of id
```

## A pseudocode algorithm for a method that solves the problem

```text
record := get student record

indexOfFirstComma := record.indexOfFirst(",")

indexOfLastComma := record.indexOfLast(",")

firstName := record[indexOfFirstComma + 1, indexOfLastComma)

firstInitial := firstName[0, 1)

lastName: = record[0, indexOfFirstComma)

lastNamePortion := lastName[0, 4)

id := record[indexOfLastComma + 1, record.length)

idPortion := id[0, 3)

return firstInitial.toLowerCase() + lastNamePortion.toLowerCase() + idPortion.toLowerCase()
```

## An alternate version

```text
record := get student record

indexOfFirstComma := record.indexOfFirst(",")

indexOfLastComma := record.indexOfLast(",")

firstName := record[indexOfFirstComma + 1, indexOfLastComma)

firstInitial := firstName[0, 1).toLowerCase()

lastName: = record[0, indexOfFirstComma)

lastNamePortion := lastName[0, 3].toLowerCase()

id := record[indexOfLastComma + 1, record.length)

idPortion := id[0, 3)

return firstInitial + lastNamePortion + idPortion

```

## A Java implementation

<https://repl.it/@jpratt/lec03MruUsernameGenerator>
