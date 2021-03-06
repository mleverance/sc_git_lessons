# Version Control with Git
---
> ## Learning Objectives 
>
> *   Understand the benefits of an automated version control system.
> *   Understand the basics of how Git works.

We'll start by exploring how version control can be used
to keep track of what one person did and when.  
Version control is one of the most important concepts we teach in SC, but Git is a complicated tool.  
Caveat: It requires time and practice to feel comfortable with it. You might leave here today thinking "this is really difficult" and that's ok.  

## Version control
Even if you aren't collaborating with other people,
automated version control is much better than this situation:

> show phd comic slide

We've all been in this situation before: it seems ridiculous to have multiple nearly-identical versions of the same document. Some word processors let us deal with this a little better, such as Microsoft Word's "Track Changes" or Google Docs' version history.  

Ask “Who uses ‘undo’ in their editor?” All say “Me”. ‘Undo’ is the simplest form of version control.

> show slide 2
Version control systems start with a base version of the document and 
then save just the changes you made at each step of the way. 
You can think of it as a tape: if you rewind the tape and start at the base document, 
then you can play back each change and end up with your latest version.


> show slide 3
Once you think of changes as separate from the document itself, 
you can then think about "playing back" different sets of changes onto the base document 
and getting different versions of the document. For example, two users can make independent 
sets of changes based on the same document, and any conflicts get resolved  

> show slide 4 - vocab

A version control system is a tool that keeps track of these changes for us and
helps us version and merge our files. It allows you to
decide which changes make up the next version, called a
[commit](reference.html#commit), and keeps useful metadata about them. The
complete history of commits for a particular project and their metadada make up
a [repository](reference.html#repository). Repositories can be kept in sync
across different computers facilitating collaboration among different people.

Questions for etherpad:  

How do you collaborate in workgroups?  
On what types of files?  
What about attrition from the group?  

