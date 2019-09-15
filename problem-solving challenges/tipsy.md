# Tip Calculator Challenge

## The problem

We want to create a method that calculates how much of a tip to give, based on a given bill total.

To make things simple, we will assume that we want to give a tip that's 15% of the non-GST portion of a bill, and that the bill total we are given does not include the GST.

For example, if we are given a pre-GST total of **10.00**, we would want our method to return **10.00 \* 15% = 1.50**.

## Generate examples to understand the problem

You should think of some example inputs and their corresponding outputs to see if you really understand what's being asked. Making examples will greatly help catching situations that need clarification.

| Input | Expected Output |
| ----- | --------------- |
| 10    | 1.5             |
| 20    | 3.0             |
| 17.34 | 2.601           |
| 0     | 0               |

| Unacceptable Inputs |
| ------------------- |
| "hi"                |
| "123.12"            |
| -41.23              |

## Assumptions/Restrictions

- the bill will be a double >= 0
- the tip will always be a fixed percent (15%)
- the amount of the bill provided does NOT include the GST portion

## A natural language algorithm for a method that solves the problem

```text
get the amount of the bill

return the amount of the bill x 15%
```

## A pseudocode algorithm for a method that solves the problem

```text
billAmtIncludingGST := get bill amount

tipAmt := 0.15 * billAmtIncludingGST

return tipAmt
```

## An alternate version

```text
billAmtIncludingGST := get bill amount

return 0.15 * billAmtIncludingGST
```

## A Java implementation

<https://repl.it/@jpratt/lec02TipsyApp>

## Some variations

_How would you approach this problem if you wanted the method to also take in a tip % (instead of defaulting to 15% all the time)? What if the incoming bill total included the GST, but you still only wanted to calculate the tip based on the non-GST portion?_
