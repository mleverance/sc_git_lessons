# Version Control with Git
---
> ## Learning Objectives 
>
> *   Understand the benefits of an automated version control system.
> *   Understand the basics of how Git works.

We'll start by exploring how version control can be used
to keep track of what one person did and when.  
Even if you aren't collaborating with other people,
automated version control is much better than this situation:

> show phd comic slide

We've all been in this situation before: it seems ridiculous to have multiple nearly-identical versions of the same document. Some word processors let us deal with this a little better, such as Microsoft Word's "Track Changes" or Google Docs' version history.

Version control systems start with a base version of the document and 
then save just the changes you made at each step of the way. 
You can think of it as a tape: if you rewind the tape and start at the base document, 
then you can play back each change and end up with your latest version.

> show slide 2

Once you think of changes as separate from the document itself, 
you can then think about "playing back" different sets of changes onto the base document 
and getting different versions of the document. For example, two users can make independent 
sets of changes based on the same document.

> show slide 3

If there aren't conflicts, you can even try to play two sets of changes onto the same base document.

> show slide 4

A version control system is a tool that keeps track of these changes for us and
helps us version and merge our files. It allows you to
decide which changes make up the next version, called a
[commit](reference.html#commit), and keeps useful metadata about them. The
complete history of commits for a particular project and their metadada make up
a [repository](reference.html#repository). Repositories can be kept in sync
across different computers facilitating collaboration among different people.

> show slide 5
