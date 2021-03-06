# Creating a Repository
---

Once Git is configured,
we can start using it.  
This lesson is using a story with three characters - the Wolfman, the Mummy, and Dracula - who are investigating if it's possible to send a planetary lander to Mars, so the files we create and text we type will relate to them.
Let's create a directory for our work and then move into that directory:

~~~ {.bash}
$ cd ~/Desktop
$ mkdir planets
$ cd planets
~~~

Then we tell Git to make `planets` a [repository](reference.html#repository)&mdash;a place where
Git can store versions of our files:  
The command `init` initializess a repository, so using the `git verb` combination, we type:

~~~ {.bash}
$ git init
~~~

If we use `ls` to show the directory's contents,
it appears that nothing has changed:

~~~ {.bash}
$ ls
~~~

But if we add the `-a` flag,  
which shows all entries starting with `.`,  
we see the current directory `.`, the parent directory `..`, and  
we can see that Git has created a hidden directory within `planets` called `.git`:

~~~ {.bash}
$ ls -a
~~~
~~~ 
.	..	.git
~~~

Git stores information about the project in this special sub-directory.
If we ever delete it,
we will lose the project's history.

We can check that everything is set up correctly
by asking Git to tell us the status of our project:

~~~ {.bash}
$ git status
~~~
~~~ {.output}
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
~~~

> ## Places NOT to Create Git Repositories
>
> Along with tracking information about planets (the project we have already created), 
> we want to track information about moons.
> We'll create a `moons` project inside the `planets` 
> project with the following sequence of commands:
>
> ~~~
> $ cd ~/Desktop   # return to Desktop directory
> $ cd planets     # go into planets directory, which is already a Git repository
> $ ls -a          # ensure the .git sub-directory is still present in the planets directory
> $ mkdir moons    # make a sub-directory planets/moons
> $ cd moons       # go into moons sub-directory
> $ git init       # make the moons sub-directory a Git repository
> $ ls -a          # ensure the .git sub-directory is present indicating we have created a new Git repository
> ~~~
> 
>
> BUT...  
> Is the `git init` command, run inside the `moons` sub-directory, required for 
> tracking files stored in the `moons` sub-directory?
> 
> > ## Solution
> >
> > No. The `planets` repository will track all files, sub-directories, and 
> > sub-directory files under the `planets` directory.  Thus, in order to track 
> > all information about moons, we only need to add the `moons` sub-directory
> > to the `planets` directory.
> > 
> > Additionally, Git repositories can interfere with each other if they are "nested":
> > the outer repository will try to version-control
> > the inner repository.   
> > 
> > Therefore, it's best to create each new Git
> > repository in a separate directory.  
> > To be sure that there is no conflicting
> > repository in the directory, check the output of `git status`. If it looks
> > like the following, you are good to go to create a new repository as shown
> > above:
> >
> > ~~~
> > $ git status
> > ~~~
> > 
> > ~~~
> > fatal: Not a git repository (or any of the parent directories): .git
> > ~~~
> > 
## How to fix a `git init` mistake
> A nested repository is redundant and may cause confusion
> down the road. We should remove the nested repository. How can we undo 
> his last `git init` in the `moons` sub-directory?
>
> > ## Solution -- USE WITH CAUTION!
> >
> > ### Background
> > Removing files from a git repository needs to be done with caution. To remove files from the working tree and not from your working directory, use the `rm` command with flags and a filename.
> > ### Solution
> > Git keeps all of its files in the `.git` directory.
> > To recover from this little mistake, we can just remove the `.git`
> > folder in the moons subdirectory by running the following command from inside the `planets` directory:  
> > But be careful! Running this command in the wrong directory, will remove
> > the entire Git history of a project you might want to keep. Therefore, always check your current directory using the
> > command `pwd`.  
> > ~~~
> > $ rm -rf moons/.git
> > ~~~
