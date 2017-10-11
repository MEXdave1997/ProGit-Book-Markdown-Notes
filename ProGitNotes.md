# ProGit Version 2 Notes

Book can be found [here][1].

## Chapter 1: History of Git
### About Version Control

___Version Control___: A system that record changes to a file or set of files over time for future recall.

#### Different Types of Version Control
___Local Version Control___: When you copy a file to a different directory. Most error prone due to probability of accidentally deleting or overwriting.

___Cerntralized Version Control___: The most common method of collaboration with version control. A sinlge sever contains all versioned files, and clients check out files from that central location.

___Distributed Version Control Systems___: Similar to the Centralized system, but the clients all have a mirror of the changes database. If the central server dies or loses data, a client can copy the data back to the server to restore it.

### How Git Came to Be.
Git started as a solution to controversy between the people behind the Linux Kernel, and a proprietary CVS called BitKeeper.

__Creator__: _Linus Trovalds_, Creator of Linux Kernel

__Release Year__: 2005

__Goals of this System__:

* Speed
* Simple Design
* Strong Support for non-linear development(branching)
* Fully distributed
* Ability to handle large projects efficiently.

### Git Basics
#### Snapshots, Not Differences
Git thinks about its data in terms of database __snapshots__ instead of as differences.

#### Nearly Every Operation is Local
Pretty much every operation in Git does not require the use of a network. This not only makes Git opreations, like looking up project history or changes, instantaneous (due to no network latency overhead), but it also allows you to do work from pretty much anywhere.

#### Git has Integrity
Everything in Git is check-summed using an __SHA-1 hash__, a 40-caharcter string made up of hexadecmal numbers (ranges 0-9 and a-f). This system lets Git be aware of any changes made to the repository. This means that you also can't lose any data via file transit or corruption without Git knowing it happened.

#### Git Generally Only __Adds__ Data
When you do something in Git, it generally only adds data in the database. There is very little that you can do that is not undoable or that can erase any data. There is a chance that you can lose/corrupt data before changes are commited, but once commited into Git, it is difficult to lose that change.

#### The Three States of Git
There are three main states within Git. Those are:
* Commited
* Modified
* Staged

__Commited__: In this state, the data is safely stored in your local/remote database.

__Modified__: In this state, Git tells you that a change has been made in a file, but you haven't saved that change within your database.

__Staged__: In this state, you have marked modified files that are ready to be placed into your next commit.

There are also three Directory Structures in Git. Those are:
* Git Directory
* Working Directory
* Staging Area

__Git Directory__: This directory is where Git stores all your references to the changes you have made on your current project. This is Gits most important part, and is what is created when you clone a copy of your project onto a different computer.

__Working Directory__: This is the single version of the project. These files are pulled out of the database (usually in a compressed format), and are placed onto the hard drive for use or modification.

__Staging Area__: This is a file that lists all the changes made which will go into your next commit.

##### General Git Workflow

Modify Files in __Working Directory__ --> Stage Files/ Add Files to __Staging Area__ --> You Commit, which will store all those changes permanently in the __Git Directory__.


[1]:https://github.com/progit/progit2
