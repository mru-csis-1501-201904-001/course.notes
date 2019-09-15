# Questionator Challenge

## The problem

We want to create a method that turns any given text into a question.

For example, if we are given the text `"This is the end."`, then we want our method to return `"This is the end?"`.

## Generate examples to understand the problem

You should think of some example inputs and their corresponding outputs to see if you really understand what's being asked. Making examples will greatly help catching situations that need clarification.

| Input                        | Expected Output              |
| ---------------------------- | ---------------------------- |
| "This is the end.            | "This is the end?"           |
| "Foo foo...!"                | "Foo foo...?"                |
| "What ho?"                   | "What ho?"                   |
| "Multiple. Sentences. Rock." | "Multiple. Sentences. Rock?" |

| Unacceptable Inputs            |
| ------------------------------ |
| ""                             |
| "huh I didn't see that coming" |
| " "                            |

## Assumptions/Restrictions

- text will have >1 non-whitespace character
- text will have >0 punctuation characters at the end
- we will only add a ? at the end of the text; if the text consists of multiple sentences, we don't change anything but the last one!

## A natural language algorithm for a method that solves the problem

```text
get the text to quesitionate

grab all the text except for the last character

return what was grabbed + "?"
```

## A pseudocode algorithm for a method that solves the problem

```text
fullText := get text to questionate

textLength := fullText.length()

textMinusLastCharacter := fullText[0, textLength - 1)

return textMinusLastCharacter + "?"
```

## An alternative version

```text
fullText := get text to questionate

return fullText[0, fullText.length() - 1) + "?"
```

## A Java implementation

<https://repl.it/@jpratt/lec02QuestionatorApp>
