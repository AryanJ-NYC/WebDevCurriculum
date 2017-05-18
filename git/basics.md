Git is version control for just about anything you write on the computer.  Since we're all developers, we'll mainly use it with respect to code.

# What is Version Control?
Version control records changes to files over time.  This allows us to take "snapshots" of our code at opportune times (when a feature is finally working, for instance).
We can create various versions of our code.  For instance, it is common for developers to have a 'master' version of their code and to write different features in separate 'branches' (separate version of code).
This gives us the power to experiment with new features while keeping our 'master' version intact.

# Why use Git?
  * It's easy to [install](https://git-scm.com/).
  * It's widely used in the development community.
  * It's open-source.
  * It lends itself nicely to collaboration.

# Common Git Commands

## [Identify Yourself](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## [Initialize a git repository](https://git-scm.com/docs/git-init)
`git init [directory]`

Initializes a git repository in [directory].  If [directory] is not specified, a new git repository is created in the current directory.

## [Add files to be staged](https://git-scm.com/docs/git-add)
`git add [<path>]`

Stages all (`git add .`)  or some files (`git add this_file.txt`) in directory.

## [Make a commit](https://git-scm.com/docs/git-commit)
`git commit [-m <msg>]`

## Create (and go to) New Branch
`git checkout -b <branch-name>`

Creates and goes to a branch of branch-name.

*Important:* Remember to run this command while in the branch you want to branch from.

For example, if you want a branch that start off looking like the master branch (common), create the new branch off the master branch.

## Go to an Existing Branch
`git checkout <branch-name>`

# Homework
1. Complete CodeSchool's [Try Git](https://www.codeschool.com/courses/try-git) course.
2. Complete Codecademy's [Learn Git](https://www.codecademy.com/learn/learn-git) course.
3. Sign up for [GitHub](http://www.github.com).

# Resources
[Git Init - Egghead Video](https://egghead.io/lessons/misc-practical-git-create-local-repos-with-git-init?course=practical-git-for-everyday-professional-use)  
[Git - The Simple Guide](http://rogerdudler.github.io/git-guide/)  
[Getting Git Right](https://www.atlassian.com/git)
