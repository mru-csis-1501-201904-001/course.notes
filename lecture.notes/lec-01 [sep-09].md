# 1501-001 Lecture Notes

## [Sep 09] Lec-01: bit of hardware, data types, jumping into Java

### a first program

- [ ] want something attention-getting, but that's too much pressure on me. I'll pick on you instead. Code at: <https://repl.it/@jpratt/lec01firstapp>
  - so what can we talk about here?
    - [ ] `Main.java`
      - [ ] **public static void main(String[] args)**
      - [ ] magic for now
      - [ ] it's where the ball starts rolling for ANY Java application, big or small
      - [ ] I do things a bit differently
    - [ ] `FirstApp.java`
      - [ ] **public** (magic for now. hang tight for a few weeks)
      - [ ] **class** FirstApp
        - [ ] naming convention => use **Pascal case**
        - [ ] the **source file name** must match the class name exactly (including case) and end in `.java`
        - [ ] must have an opening and closing brace. They're a mating pair. If you forget one, the **compiler** gets annoyed.
    - [ ] a **void** **method** called run()
      - [ ] notice how it's indented over? That's actually important.
      - [ ] a method is a named clump of one or more statements
      - [ ] don't worry about void for now - we don't have anything useful to compare it to for the moment
      - [ ] hey! More braces. How wonderful they've mated.
      - [ ] another indent! Readability rocks.
      - [ ] here comes the **body** of the method
        - [ ] **System.out.println(1);**
          - [ ] System.out is <https://docs.oracle.com/en/java/javase/12/docs/api/java.base/java/lang/System.html#out>
            - [ ] that's an example of Java API documentation - it's like the instruction manual for the Java language.
            - [ ] println is also a method (like run, in this example)
          - [ ] we say that println is being **called** here with an **argument** of 1
          - [ ] unlike the method _run_, we don't know what code is in the body of println (though we could find out!) - we just know what it does, and that's usually enough
        - [ ] let's make some errors and see what happens
          - [ ] show some **syntax errors**
            - [ ] thar's gold in them thar error message hills!
          - [ ] show some **run-time errors**
          - [ ] which type is more challenging to deal with?
    - [ ] can I get a "whew!" ... all that for 3 lines of code?!?!? (and any q's?)

### let's putz around

- [ ] let's make it TWICE as exciting: you tell me how to double it
- [ ] how about 1/2 as exciting?
- [ ] how about 1 more exciting?
- [ ] how about 3 less exciting?
- [ ] let's leave it at that for now

### pull back the curtain a bit

- [ ] unfortunately, some important things are being hidden here by REPL.IT...let's roll up our sleeves a bit
- [ ] an inviting run button is nice, but what's going on?!?
  - [ ] source files => **compiler** => **class** files (**bytecode**)
  - [ ] watch in action @ command line (need a JDK - Java Development Kit to do this, like <https://adoptopenjdk.net/index.html> ) **javac** command
  - [ ] go other way with **javap** command - hey look! Bytecode!
    - [ ] aren't you glad you don't have to program this way? some people do...who?
    - [ ] COMP2655 - whole semester
    - [ ] oh, wait - you guys, too: COMP2531
  - [ ] run the app (remember we need a public static void main - what if it's not there? let's find out!)
  - [ ] the instructions (bytecode) in the class file are run on the JVM (Java Virtual Machine), which talks to your OS
- [ ] there you have it: our first exciting piece of **software**; code that makes the computer hardware change in some way. Speaking of which...

### hardware

- [ ] this ain't a hardware course, but you should know some bits (why?)
  - [ ] **I/O** devices
    - [ ] input: examples, anyone?
    - [ ] output: examples?
  - [ ] **storage**
    - [ ] primary storage (aka RAM)
    - [ ] secondary storage (like hard drives)
  - [ ] **CPU** (aka the "brain")
    - [ ] where instructions are carried out
    - [ ] issues orders to other parts of the computer
    - [ ] can do 7 basic things:
      - [ ] read from an input device
      - [ ] write to an output device (System.out.println anyone?)
      - [ ] read a value from storage
      - [ ] write a value to storage
      - [ ] do "math"
      - [ ] branch
      - [ ] loop (i.e. repeatedly branch)
    - [ ] it's freaking insane what you get for just those 7 things

### let's play with variables of different types

- [ ] does this do the same thing? <https://repl.it/@jpratt/lec01firstappwithvariables>
- [ ] **int theExcitingNumber = 1;** does 2 exciting things
  - [ ] **declares** an **integer** **variable** named theExcitingNumber, and
  - [ ] _initializes_ that variable (to be 1)
  - [ ] could also do that in 2 steps, declaration and an **assignment** **statement** (but...)
- [ ] let's play
  - [ ] make that var 2.5x as big...oops! what happened?
    - [ ] so now we know 2 diff types: **int** and **double**
    - [ ] who can go in who? why? welcome to **casting**
  - [ ] let's get weird
    - [ ] let's look at <https://repl.it/@jpratt/lec01integerwackiness>
      - [ ] we see some **concatenation**
      - [ ] we see some // **comments**
      - [ ] take off the comments and...BY ODIN'S BEARD!!!! WHAT DEVILRY IS THIS?!?
      - [ ] let's talk about the number 1...and 0...and memory
    - [ ] let's now look at <https://repl.it/@jpratt/lec01floatingpointwackiness>
      - [ ] we'll get to those **String.format** things either Wednesday or Thursday
      - [ ] if we run it...we feel confused. What's going on?!?
    - [ ] the takeaway: representing data in limited memory in binary creates pitfalls and limitations on accuracy and what we can do
    - [ ] more importantly, you can now understand two important things

---

### Review

These are just some of the questions you should be able to answer after today's lecture; you are encouraged to make your own as well.

If you have the textbook, you can find answers to these questions in chapters 1 and 2. Use of the index will be helpful.

- [ ] what method is the entry point for all Java applications?
- [ ] what is the naming convention for Java classes? What is it called?
- [ ] what do you find in a **source file**? What extension must it have?
- [ ] how are the class name and source file name related?
- [ ] what would the contents of the source file for class Foo look like, assuming it was empty?
- [ ] what's the job of a **compiler**?
- [ ] what gets created when you compile the source file Bar.java? What's inside it?
- [ ] you've just successfully compiled Baz.java. When you run the resulting app, what happens?
- [ ] what is a **method**? What parts does it have?
- [ ] what kind of things can you do to make your code more readable?
- [ ] you want to print out the number 17 to the console. How do you do that in Java?
- [ ] why is it a good idea to read the Java API docs?
- [ ] here's some Java code: `simulateExplosion(15)`. What method is being called? What do we call the 15 here?
- [ ] what kind of errors does the compiler catch for you?
- [ ] what kind of errors do you only find when you run some code?
- [ ] what useful information can you find in a Java error message?
- [ ] what symbols do we use in Java for addition, subtraction, multiplication, and division?
- [ ] what's the job of the **CPU**?
- [ ] what are some example of **input devices**? **Output devices**?
- [ ] what are the 7 basic things a CPU can do?
- [ ] how would you declare a well-named variable that holds the number of letters in a person's name?
- [ ] what are the two numerical types that you will use most often? Why would you choose one over the other?
- [ ] we can write the decimal number 5 as 0101 in base 2. What's another name for base 2? What relationship does base 2 have with computers?

### Terms

- [ ] source file
- [ ] compiler
- [ ] compile
- [ ] method
- [ ] class file
- [ ] bytecode
- [ ] JVM (Java Virtual Machine)
- [ ] console
- [ ] syntax error
- [ ] run-time error
- [ ] CPU
- [ ] I/O device
- [ ] primary memory
- [ ] secondary memory
- [ ] type
- [ ] int
- [ ] double
- [ ] variable
- [ ] declare
- [ ] initialize
- [ ] concatenate
- [ ] cast
- [ ] argument
