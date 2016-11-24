<!--
Location: SF
Last edited by: Brianna
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Command Line Interface
![under construction](http://www.sharonkgilbert.com/wp-content/uploads/2015/12/Under-construction-1-150x150.png)

### Why is this important?
<!-- framing the "why" in big-picture/real world examples -->
*This workshop is important because:*

Most people are familiar with their computers' graphical user interface, rich with icons and buttons.   The command line interface, or CLI, is an alternative without these fancy graphics -- a plain, text-­based interface for performing tasks on a computer.

Many of the tasks developers perform are faster when done from the command line, and the command line interface usually has some extra features that are hidden in normal graphical interfaces. That's because programmers assume someone using the command line is more knowledgeable about their computer and less likely to make mistakes.  Think about that from an employment perspective, too. As a developer, you will be expected to be proficient with your computer, including performing basic tasks on the command line.

### What are the objectives?
<!-- specific/measurable goal for students to achieve -->
*After this workshop, developers will be able to:*

- Navigate the file system from the command line.
- Create, move, copy, and delete files or directories from the command line.
- Explain and give examples of flags.
- Research unfamiliar shell commands with `--help`, `man`, and/or online resources.
- Describe the uses of the `sudo` and `chmod` commands.


###Where should we be now?
<!-- call out the skills that are prerequisites -->
*Before this workshop, developers should already be able to:*

- Open a command line interface on a computer (Terminal in Mac).
- Accurately type commands into the command line interface.
- Find absolute and relative file paths.
- Navigate the file system from the graphical user interface.
- Create, move, copy, and delete files or directories from the graphical interface.


###What is the Command Line Interface?

- A CLI is a program to interact with a computer through text.  Mac's command line "shell" program is called Terminal. It lets users interact with the operating system.  It's a "Read, Evaluate, Print, Loop"-style program.

  **You do:** Open Terminal. Try using the keyboard shortcut Command + Space to search for Terminal.

- User can input commands in a specific "shell" scripting language. The default command line language for macOS and many Linux distributions is called `bash`. You may also eventually use variants like `zsh`, `ash`, `ssh`, and their predecessor `sh`.

  **You do:** In Terminal, use the `pwd` bash command.  What does it tell you?

**Check for Understanding**

1. Write down three tasks you have used Terminal for in the past.

1. Write down bash commands for each of the tasks you thought of.

*Hint*: If you're having trouble figuring out how to do something in the Terminal, try searching online for that task plus "in Terminal" or "in bash":

- "create file in bash"
- "list hidden directories in bash"

> Note: `git` commands are not part of the bash language. They use bash, and they're added separately when you install git.

###Bash Commands

On the command line, bash usually have the same structure. The base command is followed by some number of options and flags.

####Essential commands:

0. `man`

1. `cd`

2. `ls`

3. `mkdir`

4. `touch`

5. `rm`

6. `cp`


####Common Flags

The same flags won't work with every command, but knowing a few will help you decide what to look for in a new command's documentation.

1. `-r`
  - `cp -r`
  - `rm -r`

2.  `-a`
  -  `ls -a`

3. `-f`
  - `rm -f`


####Commands for permissions:

1. `sudo`

2. `chmod`

###Key Locations on the Mac

Absolute Paths:
1. `/`

2. `~`


Relative Paths:
3. `.`

4. `..`


> Note: When you're typing a file or directory name, you can hit Tab as soon as you've given the computer enough information to know which file you need. Try it!

  ```bash
  $ cd ~   
  $ ls  
  Desktop Documents Downloads
  $ cd D     # if you hit Tab after D, you may hear a beep - the computer can't tell which directory you want yet.
  $ cd De   # now Tab will fill in Desktop
  ```

### Closing Thoughts

**Review!**

1. What is `bash`?

1. What is a "shell"?

1. What extra step should you take before running a command with `sudo`?

**Put it into practice!**

1. When you need to work with your file system in WDI, use the command line.  Make `cd`, `ls`, `mkdir`, and `touch`  a part of your everyday coding habits this week.  If you feel comfortable with those already, choose a new bash command to learn.

1. Another important part of using your computer efficiently is learning keyboard shortcuts.  Make `Command Space`, `Command F`, and `Command Tab` a part of your everyday coding practice.   If you feel comfortable with those already, choose a new shortcut to learn. 

<!--
### Additional Resources

1. [In-depth HTTP Intro](http://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)
1. [Starting an Express Project](http://expressjs.com/starter/installing.html)
1. [Express Hello World](http://expressjs.com/starter/hello-world.html)
1. [Express Basic Routing](http://expressjs.com/starter/basic-routing.html)
-->
