# Setting Up Git
---

When we use Git on a new computer for the first time,
we need to configure some items, and we'll use the shell to do this.  

Commands in Git are written as `git verb`,
where `verb` is what we actually want it to do.
In this case,
we're telling Git:

*   our name and email address,
*   what our favorite text editor is,
*   how to handle line endings, and
*   that we want to use these settings globally (i.e., for every project)

Open your shell and we'll walk through setting these up
* First we'll set up our username
* We'll be using the `--global` flag to tell Git to use the settings for every project on this computer.
~~~ {.bash}
$ git config --global user.name "Vlad Dracula"
~~~
* Use the same email address you used for your github.com account
~~~
$ git config --global user.email "vlad@tran.sylvan.ia"
~~~
Now we'll set up the text editor. There are a handful of text editors that can be configured, but we're going to set up nano since we're already familiar with it.  
~~~
$ git config --global core.editor "nano -w"
~~~


| Editor             | Configuration command                            |
|:-------------------|:-------------------------------------------------|
| nano               | `$ git config --global core.editor "nano -w"`    |
| Text Wrangler      | `$ git config --global core.editor "edit -w"`    |
| Sublime Text (Mac) | `$ git config --global core.editor "subl -n -w"` |
| Sublime Text (Win) | `$ git config --global core.editor "'c:/program files/sublime text 2/sublime_text.exe' -w"` |
| Notepad++ (Win)    | `$ git config --global core.editor "'c:/program files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Kate (Linux)       | `$ git config --global core.editor "kate"`       |
| Gedit (Linux)      | `$ git config --global core.editor "gedit -s"`   |

Lastly we'll set up line endings:
> When you hit Return on your keyboard, your computer encodes this input as a character. Different operating systems use different character(s) to represent the end of a line. (You may also hear these referred to as newlines or line breaks.) Because Git uses these characters to compare files, it may cause unexpected issues when editing a file on different machines.  

On macOS and Linux:
~~~
$ git config --global core.autocrlf input
~~~
And on Windows:
~~~
$ git config --global core.autocrlf true
~~~


The commands only need to be run once, but can be changed later or as many times as you want: just use the
same commands but modify the items that were in quotes.

You can check your settings at any time:

~~~ {.bash}
$ git config --list
~~~

### Git Help and Manual
If you forget a git command, you can access the list of commands by using -h and access the Git manual by using --help :
~~~
$ git config -h
$ git config --help
~~~

