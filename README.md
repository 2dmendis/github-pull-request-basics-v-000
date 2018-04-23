<<<<<<< HEAD
# Github Pull Request Basics

## Objectives:

1. Understand what a pull request is
1. Identify how to create a pull request from one fork to another
2. Identify how to add commits to an existing pull request

## Overview:

The concept of a pull request is unique to Github. It is a request for the
owner of a receiving repository to take your changes, that you made on your
own copy of the repo ("your fork"), and "pull" them into the owner's repository.
Pull requests power the open source community. Through this process,
anyone can fork a repo, make changes and submit a pull request. Instead of
the owner working on their codebase alone, _anyone_ can contribute: tests,
documentation fixes, new features, awesome layout and graphics, etc...

There are some vocabulary words that we need to keep in mind in order to make

* **revision control system**: a software program that keeps tracks of updates /
  deletions / additions / changes to a collection of content (usually a
  directory)
* "**repository**" (or "repo"): a directory of content (including subdirectories)
  which is managed by `git` (or, "under revision control")
* "**organization**" (or "org"): a parent entity which "owns" a repo. This might
  be an organization (IBM, Microsoft, the Python foundation) or it might be an
  owning human (`sgharms`). In the case of Learn.co labs, "orgs" are
  `learn-co-curriculum` and `learn-co-students`
* "**fork**:" to make a copy of the **repository** owned by one **org** and add it
  within _another_ **org**. `sgharms` might "fork" `ruby/ruby` (that is `ruby`
  org's `ruby` repo) to his own org.
* "**clone**:" to copy a remote repo (on Github, typically, but this could be
  from a remote server, from a USB drive, even from another directory on your
  local system) to a local directory with the same name that's under git
  revision control
* "**pull request**:" to request that the owner of another org take changes you
  made to your copy of the repo and integrate it into theirs _as if_ you had
  done the work _on theirs directly_. [Here][pr] is a great example of a pull
  request on the `Ruby` codebase.

Let's go over a conceptual example. It's OK if this feels a bit confusing at
first, you'll work through this countless times and eventually your brain and
fingers will both grasp what's going on.

### Pull Request to a Source Repository

1. Suppose you "fork" a repo from `https://github.com/learn-co-students/awesome-lab`.
2. You now have a _copy_ of that repo on your Github account ("organization") i.e.
   `https://github.com/your-user-name/awesome-lab`. Technologists would say
   you "forked" the `awesome-lab` repo from the `learn-co-students` organization
   to the `your-user-name` organization.
3. But you still don't have a *local* copy of this repository on your computer.
   To do so you will...
4. Clone from **your** fork to your computer. There's no reason you _couldn't_
   clone from the _original_ repo. However, most repo owners don't want random
   people on the Internet (that's you!) committing to their repo. What you're
   going to do is establish a "parallel" repo in _your_ org and then tell the
   "source" repo "Hey, I added something awesome, I'm requesting that you _pull_
   it in."
5. Make some changes on your local machine
6. Push your code from your local system _back_ to _your_ fork
7. Create a pull request that requests your improved code be "pulled" into the
   source repo.

### Pull Request From One Fork To Another

Here's a story:

1. You fork the repository `https://github.com/learn-co-students/awesome-lab`
   to `https://github.com/your-user-name/awesome-lab`.
1. You make some changes to your newly forked repo.
1. Another student forks the repository
   `https://github.com/learn-co-students/awesome-lab` as
   `https://github.com/their-user-name/awesome-lab`.
1.  You make some changes and you want to send a pull request to their fork
    `https://github.com/their-user-name/awesome-lab`. How do you do this?

Amazingly, `git` doesn't care whether one repository is the "source" or is
"another fork of the source." Amazingly, if GitHub were to be wiped off the
earth tomorrow, local copies on hundreds of laptops 'round the world are _just
as good as the copy that GitHub_ had! This is why `git` is called a
"Distributed Version Control System." So, to share a pull request with another
student follows the same process as forking some famous project (like Ruby or
jQuery).

### Step 1

Click on the New Pull Request button.

![](https://curriculum-content.s3.amazonaws.com/gitpulls/2.png)

### Step 2

Here you can choose the base fork, which will be `their-user-name/awesome-lab`.
Then choose the head fork, which will be `your-user-name/awesome-lab`

Now click Create pull request.

![](https://curriculum-content.s3.amazonaws.com/gitpulls/4.jpg)

### Add Commits To An Existing Pull Request

Let's say you make a pull request from
`https://github.com/your-user-name/awesome-lab` to
`https://github.com/learn-co-students/awesome-lab`. Then you notice you made a
typo in your code. All you have to do is fix the typo, commit it and push up
the changes to your branch. As long as the pull request already exists, the
commits will be added automatically.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/github-pull-request-basics' title='Github Pull Request Basics'>Github Pull Request Basics</a> on Learn.co and start learning to code for free.</p>

[pr]: https://github.com/ruby/ruby/pull/1051
=======
# What is a Program?

### Objectives:

* Describe a program.
* Distinguish between interpreted and compiled programs.
* How to run a Ruby program in your terminal.
* List and describe the words that compose code: keywords, barewords, and data.
* Identify when and why errors occur in programming.

<iframe width="960" height="720" src="https://www.youtube.com/embed/P1cUm7BokaQ?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

[MP4](http://flatiron-videos.s3.amazonaws.com/ironboard/ruby/ruby-lecture-what-is-a-program/ruby-lecture-what-is-a-program.mp4)

### What's a Program?

All programs are just files on your computer filled with text. That text has a special syntax we call code. The programming language you're using defines the syntax of the code you are allowed to write. Programs are converted to [machine code](https://en.wikipedia.org/wiki/Machine_code) so that the computer can understand it.

### Interpreted vs Compiled

Depending on the programming language you're using, it will either be a [compiled language](http://en.wikipedia.org/wiki/Compiled_language) or an [interpreted language](http://en.wikipedia.org/wiki/Interpreted_language). Compiled programs will first be converted to machine code and then you will be able to run the program. Interpreted languages will be interpreted and converted to machine code at run time.

### Running a Ruby Program

Once you have a Ruby program as a file, you can run it through the Ruby interpreter to execute it. Your Ruby interpreter is accessible via the `ruby` command in your command line (assuming you have ruby installed correctly).

When you type in `ruby -v` you should see the version of Ruby you are currently running.

```bash
ruby -v
ruby 2.2.2p95 (2015-04-13 revision 50295) [x86_64-darwin14]
```

As an example, to run a Ruby program that was stored in `some-program.rb` you would simply type: `ruby some-program.rb`. 

### Words in a Program

Every word and character in a program has to be valid code for the Ruby language. Basically, every word can be one of three possible things:

1. A Ruby keyword, something that's part of the ruby language.
2. Literal data, things like "Strings" and numbers like 1 or 2.
3. Barewords you define and create, things like variables and methods.

Anything that isn't one of those is invalid and the Ruby interpreter will throw an error. 

Let's say you ran a program, and saw the following output (pay attention to the last line):

```
Programs are composed of basically three things:
A language's keywords, like 'if' or 'end' (approximately 43).
Literal pieces of data like this very sentence (or String).
Finally, barewords, or variables, that are set equal to things.
Anything that isn't one of those will cause an error.
lib/a_ruby_program.rb:23:in `<main>': undefined local variable or method `see' for main:Object (NameError)
```

That last line, `lib/a_ruby_program.rb:23:in '<main>': undefined local variable or method 'see' for main:Object (NameError)` is telling you that there was an error caused by an unrecognized word in the source of our program, more specifically on line 23.

We'll soon learn all about reading error messages.

<p class='util--hide'>View <a href='https://learn.co/lessons/ruby-lecture-intro-what-is-a-program'>What is a Program?</a> on Learn.co and start learning to code for free.</p>
>>>>>>> 466c3d3e6f934a2c44a13aee23c03d3cf333bc79
