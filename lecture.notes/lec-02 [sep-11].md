# 1501-001 Lecture Notes

## [SEP-11] Lec-02: Strings, and all the fun they bring(s)

### challenge 1 (Questionator, revisited)

- [ ] the challenge: make a method that, when given some text, turns that text into a question
  - [ ] is this problem well-specified? how can we tell?
  - [ ] keep your examples somewhere nearby...you'll need them
  - [ ] use examples to create assumptions, restrictions, and clarifications => write 'em down
  - [ ] we'll build our method in 3 steps: algorithm (natural language), algorithm (pseudocode), and Java code - testing as we go along
- [ ] step 1: algorithm (natural language)
  - [ ] what is an algorithm again?
  - [ ] **task**: build our algorithm in natural language
  - [ ] **task**: test!
    - [ ] easiest step to skip; bad idea
    - [ ] what do we test with? (hint: we've already done the hard part!)
- [ ] step 2: algorithm (pseudocode)
  - [ ] what is pseudocode?
  - [ ] what benefits does it have over natural language?
  - [ ] what problems does it pose?
  - [ ] "our" pseudocode style
  - [ ] **task**: build our algorithm in pseudocode
  - [ ] **task**: test!
- [ ] step 3: Java code
  - [ ] **action**: build the code from the pseudocode
  - [ ] final result here: <https://repl.it/@jpratt/lec02QuestionatorApp>
  - [ ] **task**: test!
- [ ] review: Java stuff covered
  - [ ] our Main / App / Utility pattern
  - [ ] method parameters
  - [ ] value returning method (compare to **void** method)
  - [ ] String type (viewable as consecutive characters)
  - [ ] substring method
  - [ ] length method
  - [ ] concatenation

### some other String methods you should Google up

- [ ] replaceAll => replaceAll is **case-sensitive**. If you don't know what that means, look it up!
- [ ] toUpperCase / toLowerCase

### you should now be ready to do these week-01 drills

- [ ] exclaimatron!!! (if you look up toUpperCase)
- [ ] acCENTmaKER
- [ ] redactor (if you look up replaceAll)

---

### Review

These are just some of the questions you should be able to answer after today's lecture; you are encouraged to make your own as well.

If you have the textbook, you can find answers to most of these questions in chapter 2. Use of the index and the Google will also be useful.

- [ ] what are some different ways we can express an algorithm?
- [ ] what is `pseudocode`? How does it differ from Java code? From natural language?
- [ ] write a cheatsheet for the pseudocode rules we've learned so far.
- [ ] what steps have we taken to solve a problem with working code?
- [ ] what do we have to define for a method to allow it to take in input when called?
- [ ] we want to make a method that returns the name of the person with the highest salary in a list somewhere. What should the `return type` of the method be?
- [ ] assume we have the `String` "foo". What is the `index` of the "f"? The last "o"? How could you grab the last two "o"s from "foo"?
- [ ] assume we have two String variables, firstName and lastName. How could we put them together with a space in the middle...and then find out how many characters are in the result?

### Terms

- [ ] pseudocode
- [ ] parameter
- [ ] argument
- [ ] String
- [ ] substring(int, int)
- [ ] length()
- [ ] concatenation
- [ ] System.out.println()
- [ ] void method
- [ ] value-returning method
- [ ] replaceAll()
- [ ] case-sensitive
- [ ] index
- [ ] toUpperCase()
- [ ] toLowerCase()
