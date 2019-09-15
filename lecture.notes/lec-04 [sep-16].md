# 1501-001 Lecture Notes

## [SEP-16] Lec-04: Java input, tracing code

We'll build our first "app" end-to-end today.

### introduce keyboard input in Java

- [ ] make a main and an App class
  - [ ] the main's only job in life is to create the App and tell it to run()
  - [ ] the App will communicate with the user and (at least for now) be in charge of input and output
- [ ] goal: prompt for a name, read it in, then say "Hi" to that user
  - [ ] `import java.util.Scanner;`
  - [ ] `Scanner keyboard = new Scanner(System.in);`
    - [ ] Scanner, like String is something you can "talk" to with methods (like "foo".length()). We say Scanner and String are `reference types`.
    - [ ] compare to int and double, which are kinda "dumb". We call them `primitive types`.
  - [ ] prompt (suggest using print, not println)
  - [ ] `String name = keyboard.next();`
    - [ ] what if there are spaces in the name?
    - [ ] nextLine()

### the challenge: MRU username creation

- [ ] introduce problem
  - [ ] **task**: write down some examples
- [ ] **[3 minute timer] task**: create a natural language algorithms (groups of 3)
  - [ ] **task** test by walking through examples
- [ ] **task**: convert to pseudocode
  - [ ] introduce indexOfFirst, indexOfLast
  - [ ] **task**: test by doing a trace with some of our examples
- [ ] **task**: convert to Java
  - [ ] introduce indexOf, lastIndexOf
    - [ ] if you want to use these instead of indexOfFirst/Last in pseudocode, that's cool
  - [ ] **task**: test by running some of our examples; we'll need to create a simple App class to do this

---

### Review

- [ ] what do we need to do to get keyboard input in Java?
- [ ] how does next() treat white space characters? How about nextLine()?
- [ ] you want to get a person's full name from the keyboard; which Scanner method should you use?
- [ ] what happens when you do a nextLine() right after a nextInt()/nextDouble()?
- [ ] why is using a println() a prompt not ideal? What should you use instead?
- [ ] what is a powerful technique that you can use to understand how code works and to solve run-time errors?

### Terms

- [ ] Scanner
- [ ] System.in
- [ ] import
- [ ] next()
- [ ] nextLine()
- [ ] nextInt()
- [ ] nextDouble()
- [ ] primitive type
- [ ] reference type
- [ ] trace
- [ ] newline character
- [ ] white space character
- [ ] utility/helper class
- [ ] prompt
