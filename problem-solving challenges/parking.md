# Parking Cost Calculator Challenge

## The problem

We want to make a method that calculates how much you would have to pay to park in Calgary's Surface Lot 3 (Sunalta). Parking rates are [here](https://www.calgaryparking.com/documents/10184/2114864/RateSheet_SurfaceLots_2019.07.25.pdf/1980101e-91a7-449b-ae55-139100865d18).

To make things simple, we will assume that we're only concerned with parking between 06:00-18:00, Monday through Friday. We'll also assume input will be a whole number of minutes parked.

For example, if we are given **31** as the input, then we want the method to return **2.50**. (Do you see why?)

## Generate examples to understand the problem

You should think of some example inputs and their corresponding outputs to see if you really understand what's being asked. Making examples will greatly help catching situations that need clarification.

| Input | Expected Output |
| ----- | --------------- |
| 1     | 1.25            |
| 29    | 1.25            |
| 30    | 1.25            |
| 31    | 2.50            |
| 60    | 2.50            |
| 210   | 8.75            |
| 240   | 9.00            |
| 600   | 9.00            |

| Unacceptable Inputs |
| ------------------- |
| -12                 |
| 720                 |

## Assumptions/Restrictions

- the input will be in whole minutes >= 0
- if the number of minutes is even _1 minute_ over a given ½hr, that is considered an _additional_ ½ hr
- no input would take the parking time outside the daytime hour span (06:00-18:00, weekday)

## A natural language algorithm for a method that solves the problem

```text
get the number of whole minutes parked

calculate the number of 1/2hrs from the number of whole minutes

return the maximum of 9 and (number of 1/2hrs x 1.25)
```

## A pseudocode algorithm for a method that solves the problem

```text
wholeMinutesParked:= get whole minutes parked

halfHoursParked := ceiling(wholeMinutesParked / 30)

standardCostToPark := halfHoursParked * 1.25

return max(9, standardCostToPark)
```

## An alternate version

```text
wholeMinutesParked:= get whole minutes parked

halfHoursParked := ceiling(wholeMinutesParked / 30)

return max(9, halfHoursParked * 1.25)
```

## A Java implementation

<https://repl.it/@jpratt/lec03ParkingCostCalculator>
