<!---
{
  "id": "8d3e51c2-4811-4275-976c-04e3b3215998",
  "depends_on": [],
  "author": "Stephan Bökelmann",
  "first_used": "2025-03-30",
  "keywords": ["bash", "Linux", "basics"]
}
--->

# Using the Linux Terminal

## 1) Introduction
Today most people are used to work with _graphical user interfaces_ (GUIs) on their computers.
Using the terminal is a fundamental task, that can make a developers life easier. 
While GUIs provide opportunities in terms of explorability of programs, finding new functions and playing around - terminal interfaces can help understanding the exact calls that are being made to a machine.
In addition, workflows in a terminal are usually easier to reproduce, since the only input you need can be written down explicitly.
Rather than trying to explain to someone where exactly a button is located on the screen, which also may vary from version to version and resolution to resolution, a simple line of text is enough to run a specific command. 

---

The terminal is actually called a terminal-emulator, since its purpose is to mimic the older terminal stations.
One of these terminal stations is the [Teletype 33](https://en.wikipedia.org/wiki/Teletype_Model_33).
Being one of the first devices to empoly the _ASCII_ standard encoding, published in 1963, and coming at a relatively low price, $1,000 (in 1963 USD), it quickly turned into the standard input/output for the upcoming minicomputer.

<details>
  <summary>Teletype</summary>

  Want to learn more about the Teletype? Check out [this TTY exercise.](www.github.com/STEMgraph/missing)
  
</details>

---

Imagine a computer to be more of a general purpose calculator in the beginning of computing. 
Over a terminal, two numbers are punched in, the `Enter`-key is pressed, the computer maps the two inputs onto an output and sends the series of pulses of the result back to the terminal. 


### 1.1) Further Readings and Other Sources (Linux / Bash)

- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/bash.html) – The official and comprehensive Bash reference.
- [LinuxCommand.org – Learn the Linux command line](http://linuxcommand.org/lc3_learning_the_shell.php) – A beginner-friendly introduction to Bash scripting and CLI usage.
- [Bash Guide for Beginners](https://tldp.org/LDP/Bash-Beginners-Guide/html/) – Published by the Linux Documentation Project, great for newcomers.
- [Explainshell](https://explainshell.com) – Paste a command and get explanations for each part of it.
- **Book**: Machtelt Garrels. *Bash Guide for Beginners* – Available online and free to download.
- **Book**: William E. Shotts. *The Linux Command Line: A Complete Introduction* – Excellent beginner-to-intermediate guide (No Starch Press).
- **Video**: [Linux Terminal Full Course - Basic to Advanced](https://www.youtube.com/watch?v=oxuRxtrO2Ag) (freeCodeCamp)


## 2) Tasks (Linux Edition)

1. **Open your Terminal**: Press `Ctrl + Alt + T` on your keyboard or search for "Terminal" in your system's application menu. This will open a shell window, typically running the Bash shell. You're now in a _Command Line Interface_ (CLI), which gives you text-based control over your operating system.

2. **Defining a Variable**: Type `num=5` and press `Enter`. The shell will now associate the variable `num` with the value `5`. Variables in Bash do not require explicit declaration.

3. **Print a Variable's Content**: Type `echo "$num"` and press `Enter`. This will print the stored value of the variable `num`.

4. **Pay Attention**: Type `echo num` into the shell. It will simply print the characters `num`, not the variable’s value. Use the `$` prefix and quotes to access variable contents.

5. **Calculate a Sum**: Use the `expr` command to perform arithmetic: `expr "$num" + 3`. This prints the result of the addition.

6. **Try out other Calculations**: Try out other operators with `expr`, such as `*`, `-`, `/`, and `%`. For multiplication, you need to escape the asterisk: `expr "$num" \* 2`.

7. **Setting a Result Variable**: Store results in new variables:
   ```bash
   res=$(expr "$num" + 5)
   res2=$(expr "$num" + "$res")
   ```

8. **Test a Condition**: Run an if-statement:
   ```bash
   if [ "$res" -eq 10 ]; then echo "Great!"; fi
   ```

9. **Repeat an Operation**: Use a loop:
   ```bash
   for i in {5..10}; do echo "$i"; done
   ```
   Change the numbers to explore how the loop behaves.

10. **Persistence**: Close the terminal and reopen it. Type `echo "$num"`. Nothing will appear, because Bash variables are temporary by default.

11. **Puzzle**: Initialize a variable called `Gauss` with value `0` and compute the sum from 1 to 100 in one line:

> Bonus: Try replacing `{1..100}` with `$(seq 1 100)` to see another common idiom in Unix-like systems.


## 3) Questions
1. What advantages does using the terminal offer compared to graphical user interfaces?
2. How can terminal commands improve reproducibility in software development?
3. Why can it be important to understand basic terminal operations, even when working mostly in GUI environments?
4. In what ways does using a terminal strengthen your understanding of how an operating system works?
5. Why might automation be easier with terminal tools than with graphical interfaces?
6. How can learning the terminal help you troubleshoot problems more effectively on your computer?

## 4) Advice

Don’t be intimidated by the terminal—it’s one of the most powerful tools at your disposal. Every Bash user starts with simple commands like echo or ls. Use man, --help, and tldr to explore commands, and don’t be afraid to experiment in a safe environment. Scripting simple routines can save you hours of repetitive work and deepen your understanding of how Linux works under the hood.

> "Controlling complexity is the essence of computer programming."
> — *Brian W. Kernighan*


<details>
  <summary>Windows</summary>

  Checkout the [Windows CMD](https://github.com/STEMgraph/0508295d-de49-4a67-8113-efebffc62d96) exercise as well to see the differences and similarities!

</details>
