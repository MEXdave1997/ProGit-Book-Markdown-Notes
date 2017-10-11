# Pro Git Version 2 Notes

Book can be found [here][1].

## Chapter 2: Git Basics
### Getting a Git Repository
There are 2 ways to get a Git Repository. You can either take an existing project and track it with Git or you can clone an available repository from another server.

#### Initializing a Repository in an Existing Directory
To start tracking an existing project with Git, go into the projects directory in your terminal and type

```
$ git init
```

This command creates a ```.git``` repository that contains all the files needed by your repository. At this point, nothing is being tracked by Git yet. To start version controlling your files, start an initial commit by running these commands in your terminal.

```
$ git add [whatever files you want to start tracking]
$ git add LICENSE
$ git commit -m '[your initial commit message]'
```

#### Cloning an Existing Repository
In order to get a copy of an existing Git repository, you use the following commands:

```
$ git clone [url of the repository's location]
```

This command creates a directory named after the ending of the url. For example, when running:
 ```
 git clone https://github.com/libgit2/libgit2
 ```
 the directory will be named `` libgit2 ``. To change the name of the directory created by Git, run ```clone```  with the name of the directory after it, like so:

 ```
 $ git clone [url of directory's location][desired directory name]
 ```
 Git can use several protocols. Some examples include:

##### __HTTPS:__
 * ``https://``

##### __SSH:__
 * ``git://``
 * ``user@server:path/to/repo.git``

## Recording Changes to the Repo
After you have a working Git repository, you need to commit snapshots of changes you have made and has reached a state you want to save/

As files are edited, Git detects them as __modified__, because they have been changed since the last snapshot. Files can also be either __unmodified__ and __untracked__.

The tool in git to help keep track of these files is the status tool, and can be invoked by running:

```
git status
```

Output looks something like this:

```
On branch [current working branch]
Your branch is [up-to-date/ahead/behind] with [current remote branch]
nothing to commit, working directory clean
```

Above output is displayed upon

[1]:https://github.com/progit/progit2
