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

Many of the tasks developers perform are faster when done from the command line, and the command line interface usually has some extra features that are hidden in normal graphical interfaces. That's because programmers assume someone using the command line is more knowledgeable about their computer and less likely to make mistakes.  Think about that from an employment perspective, too - as a developer, you will be expected to be comfortable performing basic tasks on the command line.

### What are the objectives?
<!-- specific/measurable goal for students to achieve -->
*After this workshop, developers will be able to:*

- Navigate the file system from the command line.
- Create, move, copy, and delete files or directories from the command line.
- Explain and give examples of flags.
- Research unfamiliar shell commands with `--help`, `man`, and/or online resources.
- Describe the uses of the `sudo` and `chmod` commands.


### Where should we be now?
<!-- call out the skills that are prerequisites -->
*Before this workshop, developers should already be able to:*

- Open a command line interface on a computer (Terminal in Mac).
- Accurately type commands into the command line interface.
- Find absolute and relative file paths.
- Navigate the file system from the graphical user interface.
- Create, move, copy, and delete files or directories from the graphical interface.


###shell

`shell command move file`

`shell command change permissions`

### Command Space, Command Tab, Command F

# How to access the command line

**In Mac OSX**: Go to /Applications/Utilities and click on "Terminal" or search for "Terminal" in Spotlight.


# A little more detail
Commands generally take the format:  

```bash
[name of the command] [option] [option] [option]...
```  

The prompt will also show what directory you're currently sitting in. Whenever you execute a command, you do it from a particular directory. This matters because when you execute a command that involves a filename or a directory name, you can specify it one of two ways:


###Relative Paths
Specifying a file or directory as a relative path means you are specifying where it sits relative to the directory you're in. For example, let's say
you're in the `videos` subdirectory of the `files` directory. You'll see this prompt:

```bash  
/files/videos$  
```  

If you execute a command like `touch newfile.txt` , it will create newfile.txt inside the current directory. Relative paths don't start with a slash.  

###Absolute Paths
Specifying a file or directory as an absolute path means you are specifying where it sits on the computer in absolute terms, starting from the top
level. For example, let's say you're in the `videos` subdirectory of the `files` directory again.

```bash
/files/videos$  
```  

If you execute a command like `touch /files/music/newfile.txt` , it will create newfile.txt inside a different folder, the `music` subfolder of the
`files` folder. *Absolute paths start with a slash.*  

If you use an absolute path, the command will do the same thing no matter what directory you execute it from.  

So, if you type:  

```bash  
/files/videos$ rm video.mp4  
```
This will delete video.mp4 from the current directory. But you would get the same result from:  

```bash
/files/videos$ rm /files/videos/video.mp4
```  

This will delete video.mp4 from the /files/videos/ directory, which happens to be the current directory.  

These two commands will not have the same result if you are in a different directory:  

```bash
#This will try to delete the file video.mp4 from the 'text' subdirectory instead, because that is the current directory
/files/text$ rm video.mp4

#This will delete the file from the /files/videos/ directory, even though it is not the current directory
/files/text$ rm /files/videos/video.mp4
```  

Remember:  

**Starting a path with a slash** means you want to give the entire path and ignore what directory you're currently in. Not starting a path with a
slash means you want to give the path starting from the directory you're in.  

If you're ever unsure of what directory you're in, you can use the `pwd` (Print Working Directory) command to get the absolute path of the current directory.  

```bash
~$ pwd
/Users/Noah
```  

##File Patterns
In most cases when you have to specify a file name or folder name, you can also specify a general **pattern** that might match multiple files. There are lots of ins and outs with this, but the most basic version is using the asterisk (*), which matches anything. It's also known as a wildcard.  

```bash
#Delete any file in the current folder
/files$ rm *
#Delete any file that ends in '.txt'
/files$ rm *.txt
#Delete any file that starts with 'data'
/files$ rm data*
```  

##Navigating
The two core commands for navigating what folder the prompt is in are `cd` and `ls`.  

`cd` stands for "Change Directory" and must be followed by a directory you want to change to. You can supply an absolute or relative path.  

```bash
#This will put you in /files/videos
/files$ cd videos
#This will put you in /videos
/files$ cd /videos
```  
You can jump multiple levels at once if you want.

```bash
#This will put you in /files/videos/short
/files$ cd videos/short
```  

You can use `cd..` to move up one level to the parent directory.  

```bash
#This will put you in /files
/files/videos$ cd ..
```
`ls` will list the files in the current directory. It's helpful for figuring out where you are, what files exist, and what subfolders exist.  

```bash
/photos$ ls
thumbnails photo1.jpg photo2.jpg
```  

Using `ls­ -l` will print the list vertically, with lots of other extra information about the file size, permissions, and last modified date:  

```bash
/photos$ ls -­l
­-rw-­rw-­r -- ­1 noah noah 58133 Oct 22 17:13 photo1.jpg
-­rw-­rw-­r­­ -- 1 noah noah 75640 Oct 22 17:13 photo2.jpg
drwxrwxr­-x  2 noah noah 4096  Oct 22 17:13 thumbnails  
```  

When typing in a folder or file name, you can hit the 'Tab' key to autocomplete if it's possible. For example, in the /photos folder, if you type in:  

```bash
/photos$ cd thu
```  

and hit 'Tab,' it will fill in the rest and show you:  

```bash
/photos$ cd thumbnails
```  

However, if there is more than possible file/folder that matches what you've typed so far, it won't work. If you type:  

```bash
/photos$ rm pho
```  

and hit 'Tab,' nothing will happen because you could be on your way to `photo1.jpg` OR `photo2.jpg`.  





### Closing Thoughts

* Use dynamic url parameters, like `/api/burgers/:index` and `/api/tacos/:index`, to request data about a specific resource. Access them on the server in the `request.params` object.
* Use query string parameters for dynamic requests to serve up dynamic responses. Access them on the server in the `request.query` object.
* Use `POST` with named form inputs to send data to our Express servers, and use `body-parser` to access that data as part of the `request.body` object.

This will be essential knowledge for building and interacting with applications that contain multiple resources.  

We'll use `PUT` or `PATCH` to send data to update item information on the server side (instead of `POST`), and we'll use `DELETE` to delete items on the server side.


### Additional Resources

1. [In-depth HTTP Intro](http://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)
1. [Starting an Express Project](http://expressjs.com/starter/installing.html)
1. [Express Hello World](http://expressjs.com/starter/hello-world.html)
1. [Express Basic Routing](http://expressjs.com/starter/basic-routing.html)
