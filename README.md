# Git & Github:  A Web Dev Newbie Guide
or how Git became less of a git


## Summary
If your new to programming or web development then this guide is aimed at you. For starters you do need to know how to use Git !  Of course like me you probably heard about Git and Github but put off learning it because its yet another layer off stuff to get your head around and you can code on your own perfectly well without using it. But learning Git is necessary because its:

   * Professionals use all the time; your expected to know it!
   * Designed for very small and very large projects
   * Zero cost: Git is free and Github if free if your code is open to public access

### This guide is for newbies and community teams
This guide is aimed at web dev newbies; those that are just getting into the technology. If your not a web dev newbie but want to review Git/Github then you might still want to read because I’ve tried to make it as straight forward as I can. And if by chance your a Git expert and you’ve stumbled upon this please feel free to offer any suggestions or corrections.
This course is also intend for those setting up community based project teams perhaps with inexperienced developers from different backgrounds. As such I aim to be as platform agnostic as I can i.e. suitable for Mac, Windows and Linux.


## Part 1: Introduction
### What is Git?
According to git-scm 
> “Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.” 

Ok so that all makes sense then my fellow newbies...er probably not.


### What does the name ‘git’ mean? something technical perhaps ?

Short answer; no. Indeed as a Brit myself it came as a bit of a surprise that it was named by its inventor Linus Torvalds as a play on the fact that people might call him a bit of a ‘git’. This is British slang for a troublesome annoying person. Thus no technical meaning, fancy mnemonics or otherwise to the actual name ‘git’. 

#### SO WHAT THE HECK IS GIT and GITHUB ?:-

>**Git** is a tool you install on your own computer for organising the development of code and communicating to programmers efficiently.

>**Github** is a cloud based version of Git that also provides repositories where code is stored and also tools to facilitate communication between coders. It is ostensibly a cloud based implementation of Git.

###A mental model of Git for newbies
Lets give you a mental model. A traditional paper office desk can become incredibly untidy and when you've run out of piling up the paper on the desk you start to pile it up un the floor, boxes, post-it notes, envelopes folders etc etc. (I’ve even known someone who had a pair of boots hidden in a pile of papers that had a mouse nesting in them!) Finding information, remembering what and who it was for can become practically impossible. 

What do you do traditionally in the paper office to keep the information organised? Well you put paper in folders, then put labels on the folders, then put the folders in cabinets which act as a storage or repository for all the information. Good so far.

![folders analogy](./images/folders_pic.jpg =350)

But here’s the problem; they are your folders, your master projects, and you need to control and manage the flow of information contained in the master folders. Now what if someone wants to amend a folder? They have to physically come to your office and perhaps sign a receipt or log-book before taking the folder away. You then rely on them keeping it in order and not adding incorrect information. One solution is that they clone the entire folder using a paper scanner, but would they would still need to put in a request to you to have any changes pulled back into the original ‘master’ folder for those changes to become ‘official’. The paper and information just logging and controlling the flow of the different copies of your folders and requests to add and take folders away itself has to be managed!


Thus the real problem is managing the flow of information in an easy way that allows people to use the master ‘folder’. Ideally people should be able to make a copy or ‘clone’ and experiment with it in a sort of separate side-branch to the master. Then when its appropriate they can request any changes be pulled back into the original. Moreover an easy way to communicating information like requesting to pull in new changes into the original that didn't rely on multiple communication channels like emails or post-it notes would be highly advantageous.

Thats what Git and Github combined together are for, only your doing things electronically of course not with real paper, but the same mental model applies.

### Keeping code organised

#### The very old way
One way of designing code is to constantly re-save your code with different version numbers onto a directory. Thats like having a filing cabinet with lots of folders, each folder representing a version of the code. But just like the paper analogy, there’s no easy method to collaborate, share code and keep track of which folder is ‘the’ master one. Your controlling the flow of information about the different copies and versions properly. This is like the folders in the cabinets model.

#### The old way of version control
The idea here is to have one central master version. Everyone project member can log into it but only one person at a time can make changes. However if the physical central server that holds the master dies then thats it, you've lost your master. This is called a ‘single point of failure’ Moreover communication is still an issue. This is like the old paper tracking method, with a log-book and one official master. This version control method is known as Centralised Version Control and its no longer the favoured way of doing version control. 

#### The modern way of version control: Git
Everyone on the project has a clone of the remote ‘repository’ where the code is stored on their local machine; yes everybody. This cloned repository (or just ‘repo’) is a clone of the programming code and also a clone of the organising information to control the project information flow. Typically a cloud based server like Github acts as the the remote repository (or just ‘remote’) for the project.
Now if something goes wrong in the remote repository, the remote master can be reconstructed from everybody's local clone. There is now no central point of failure.  Moreover cloud based remote repositories like Github don't just store the code, they provide a means to communicate between programmers and thus the information flow about the project is greatly automated and eased.

But is gets even better, because not only does each programmer have a local clone on their machine, they can also create ‘side-branch’ versions of the code to experiment with. This side-branch or just ‘branch’ isn't part of the main repository on their local machine so it doesn't effect anything else. Using branches new features can be developed with no fear of messing up either the local master copy or anyone else's master. Moreover that branch can also be communicated to other programmers to experiment with, again without messing up their main master code. Finally when this branch code behaves as desired its author can officially request that the branch be merged into the master by issuing a request to pull the branch into the master branch. The ‘pull-request’ itself is part of the communication tools available on Github. Now not only is code experimentation de-risked, but also the information flow and communication between coders is now easily managed!

Ok, lots to take in so you might want to read the last few paragraphs again, they are the nub of what Git is and why its used. Generically this type of version control is called Distributed Version Control and is the most popular form of version control now. 
A nice 2 min video here on [Centralized vs Distributed Version](https://www.youtube.com/watch?v=_yQlKEq-Ueg)


## Part 2: Choosing a suitable Git GUI
### Command line blues
As well see later in this guide, many courses online focus on using Git in the command line. However not everyone is happy learning command line approaches. Whilst personally I don’t mind using a terminal and command line, for the benefit of any experts that may be reading this let me repeat that; normal people don’t like using the command line. Given that our visual cortex is rather a big chunk of our brain, a GUI version of Git may well be understood more easily. The task is to get stuff done in git after all.

### Community Team needs
There are a lot of Git GUI front ends available for a quick reference see [“Git-scm GUI Clients”](https://git-scm.com/download/gui/linux or perhaps) [“10 Best Graphical Git Clients for Developers”](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html)
However for the purpose of this course I’ve aimed this at web dev newbies and community teams that need to cater for all platforms, not just the latest and greatest Windows or Mac. Its important to 

Questions we might ask ourselves when choosing a Git GUI might be ?
   * What platforms (Linux, Mac, Windows) are the team members using ?
   * What any new team members might use in future ?
   * How important is it thats its open source ?
   * Does it need to be entirely free to use or free for just say community projects only ?
   * Is is popular in a commercial setting does it need to have command line access or can it be just be purely GUI focused?

Our clubs aim is to develop community projects and support newbies developing skills in a professional setting. Teaching one another is important; hence having the same Git GUI may well be advantageous. Projects will be community focused and need to be have as low as possible entry costs. Moreover we have no control over what platform future team members will be joining with.

   * Needs to support all platforms as Linux is a good free fall back option

   * Command line access would be great, but perhaps not essential; one can always use the terminal

   * Open source is great, but it must work well for newbie members

   * It needs to be largely free, using the free version of a free/pro-paid business model is probably ok

Reviewing

  * [“Git-scm GUI Clients”](https://git-scm.com/download/gui/linux)

  * [“10 Best Graphical Git Clients for Developers”](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html)

  * [“Alternatives to SmartGit for all platforms”](http://alternativeto.net/software/smartgit/)
  



#### A simple table for Git GUI candidate table may be created


  
           |Github Desktop|SourceTree|SmartGit|GitKraken |Git-cola|
-----------|--------------|----------|--------|----------|--------|
Open Source|      No      |    No    |   No   | No(see 5)|   Yes  |
Free for community use|Yes|Yes|Yes (non-commercial)|Yes|Yes |
Free for professional use|Yes|Yes (need to register)|No (pro $7/mth)|No (pro $6/mth)|Yes|
Used in professional settings|Yes|Yes||Yes|unsure|
Considered easy to use|Yes|Yes (see 1)|No (see 4)|unsure|No(see 6)|
Can use command line entry|No|Yes|Yes|No|Yes|
Mac|Yes|Yes (see 2)|Yes|Yes|Yes|
Windows|Yes|Yes|Yes|Yes|Yes|
Linux|No|No|Yes|Yes (deb/Ubuntu)|Yes|


  1 [“Perfect for beginners”](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html)

  2 [“What are the other differences between the Mac version and the Windows version: As at the time of writing (version 0.8b) ... features from the Mac version are missing from the Windows port….{including} Listing & creating projects on Bitbucket, Stash and GitHub”](https://www.sourcetreeapp.com/faq/)

  3 “A purpose is non-commercial only if it is in no manner primarily intended for or directed toward commercial advantage or private monetary compensation.
  Examples of non-commercial purposes:you are using the SOFTWARE to work on open-source projects….Examples of commercial purposes, i.e. when you will need a Commercial License:...using the SOFTWARE in your spare time to manage the website source code of your local football club and you are getting paid for that.”

  4 [“best suited for professional teams working on big projects”](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html)

  5 [“How can I open the command line from GitKraken?: GitKraken is not a front-end GUI for your command line; it’s a 100% standalone application”](https://www.gitkraken.com/faq)

  6 [Git-Cola:](http://git-cola.github.io) is [“ideal for power users and tech ninjas”](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html) It’s easily available in Linux based software repositories, I’ve installed it both on Linux Mint and KDE Neon and KaOS (admittedly all Ubuntu based distros) but with no problems.  Git-cola comes in two parts, the main ‘cola’ part that lets you do commands like commit see the console and status etc, and the ‘DAG’ drawing part which shows the log history and a graphical representation of the branching. Its an excellent endeavour from its creators however from a newbie perspective perhaps not polished enough as of 2016, for example it would seem you still need to initialise a repository using the command line.




### Comparison of candidate GUI’s
Having picked candidate GUI’s, the truth is that there isn’t a perfect solution for a newbie team that need to use all platforms and ideally support open source.  All the GUI’s require Mac 10.9 or Windows 7 and above so those on a tight budget might be left out. However one could install a free Linux Debian/Ubuntu distro and switch to GitKraken which might be acceptable for newbies or push comes to shove, then back to the command line which might not be a bad thing.

Hence the best fit GUI options seem to be SourceTree or GitKraken which aren't open source unfortunately but are used in a commercial context so having experience with them is useful nevertheless. SourceTree and SmartGit seem polished and professional but SourceTree liscence appears to be less restrictive than SmartGit.

A switch to git-cola might make sense as its both open source and platform agnostic but it seems to be geared for experts both on installation and usage. Also its not clear how popular it is in a commercial setting compared to say SourceTree which looks newbie friendly but also very professional in terms of documentation for example.

SourceTree would come out on top as it has great documentation and command line support but its biased more towards Mac at the moment and frustratingly isn’t on the Linux platform.
For the reasons above a combination of GitKraken and the command line using the terminal are what are suggested at this point in time. Experimentation may counter my arguments above but its a reasonable starting point. All team members should be able to use this software, even if they have to install Linux if a Windows 7 upgrade isn’t feasible for instance if they are using an older machine (as I sometimes do).

Bottom line if most people are Windows/Mac focused then SourceTree or Github Desktop are safe bet. Linux users could just stick to the command line? However for maximum platform flexibility, and a newbie friendly Git GUI for as wider inclusivity community team as possible then GitKraken is probably a good starting point, perhaps ‘the’ only choice at time of writing (though I really wish the SourceTree was on Linux)

### Conclusion
We’ll go with GitKraken as a Git GUI for now.

Note: Why Github who created the brilliant platform agnostic Electron desktop application software can’t make Github Desktop a platform agnostic Electron app, yet Axosoft can create GitKraken using Electron baffles me? From Github’s FAQ [“Q: Why don't you support the Linux platform? A: At this time, we're focused on optimizing the Mac and Windows experience. We're always thinking about potential improvements for the diverse needs of our users, though!”](http://bit.ly/2biq72V) 









## Part 2: A review of online courses on Git
## Command line focused
Several free popular online courses on Git (though Code School has a paid ‘pro’ version) and all of them focus on using the command line are:

  * [Code School ‘Git real’](http://gitreal.codeschool.com)
  
  * [Nodeschool ‘Git-it’](https://github.com/jlord/git-it-electron) (the new Electron desktop version)
  
  * [Udacity ‘How to Use Git and GitHub’](https://www.udacity.com/course/how-to-use-git-and-github--ud775)
  
Learning is a very personal thing and the main take-away I got from these courses was that no single one ‘did it’ for me, but they all enhanced my understanding and were well constructed. It took a number of sessions before Git reasonably ‘clicked’.
Typically one has to do a course a number of times or do a couple of different courses presented in different ways for Git to resolve in ones mind. Remember its not time wasted, Git is ubiquitous in the coding world.


#### [CodeSchool: TryGit:](https://try.github.io/levels/1/challenges/1) 
“Got 15 minutes and want to learn Git?” This is the strap-line for TryGit. 
I’d strongly urge you to do this course first simply because its an excellent 15 minutes well spent. It’s feature on the [Git website itself](https://git-scm.com)
Codeschool also have made more in-depth Git courses including “Git real” 
  
  
#### [‘Git real’](http://gitreal.codeschool.com)
Time to do course: approx 3 hours
CodeSchool do a fantastic job of making an otherwise dull subject actually seem exiting ! There videos are far from dull and get across the key points well. Added to that you can download the video as a pdf of slides.


#### [gitReal 2 is also worth looking at](http://gitreal2.codeschool.com/levels/1) 
for more advanced users. With Code School you have a simulated Git terminal that you enter your commands into. Though it works very well, perhaps it would be nicer to actually install Git and use a real Github account as part of your learning curve. That quibble aside, it’s well worth doing this course.


#### [Nodeschools ‘Git-it’](https://github.com/jlord/git-it-electron)
(the new Electron desktop version) Time to do course: 1 hours I’d very much recommend doing this course because its an app that you download. You can keep the app an your desktop an dip into the course if your memory goes, plus its not too long to do 

Git-it itself is open source and it’s stored in a public access repository. Any coder may contribute to it on Github. [Some instructions on how to download and install Git](https://github.com/jlord/git-it-electron/issues/121#issue-149747488)

Versions for 64bit Mac (44.3 MBGit-it-Mac-x64.zip), Windows (117 MBGit-it-Win-ia32.zip) or Linux (Git-it-Linux-x64.zip) [may be downloaded](https://github.com/jlord/git-it-electron/releases). I’ll be using this course as a frame to my own Git tutorial also including the use of the Git GUI Gitkraken (see below).


#### [Udacity ‘How to Use Git and GitHub’](https://www.udacity.com/course/how-to-use-git-and-github--ud775) 
Time to do course: approx 18hrs This is the longest course on the list by far, but I definitely would recommend you do it if you can spare the time. Udacity has a slightly more academic way of covering topics. Thats not to say its irrelevant, it just less ‘wham-bam’ more get your brain in gear then step-by-step.

Udacity always provide excellent video and course note downloads plus other resources. In this course one of the most valuable bits for some might be the ‘concept maps’ used to build up a picture of where all bits of Git fit in

Another nice touch to the course is that they you use reflective learning techniques in the course. As you go along you save your thoughts in a simple .txt log and these become versions that you store in Git itself, giving you even more practice.

Udacity regularly asks questions and provides quite good automated feedback on your answer.
One minor irritation is a couple of times you have to download and install a file to simulate a commit from someone or to simulated Github repository activity. Whilst the idea is sound, its quite distracting and I hope Udacity tweaks this part of the course in future to make the lesson closer to the real thing.

### Which course would I recommend? 
Much depends on the environment your learning in, time availability etc. If push came to shove and your very short on time I’d say do the nodeschool “git-it” course. However if your like me and the fast pitch approach isn’t enough to stick in your head then add in the Udacity course or the Git-real course from CodeSchool.Notable Quality Youtube Tutorials 

Youtube provides some excellent tutorials including: 

  * [“GitHub for Noobs” by Travis Neilson](http://bit.ly/2buQQ9Z)
Travis is a front-end developer with a superb channel aimed at the creative arty types who also need to do coding. He now works for Google and has presented some videos on Adobe’s channel. If your a ‘creative’, as in art, that needs to code his channel he’s a great starting point. He presents in a very entertaining and articulate way four videos 5 to 25 minutes each.

  * [“Git Video Tutorial” by Derek Banas](http://bit.ly/2aYkkyw)
If you like a fast pace, and your into coding then Derek’s your guy. Have a look around his channel and you'll be impressed by the breadth of his knowledge on coding.  His Git courses is four videos approx 15 to 25 mins each.

  * Github themselves have produced Git and Github tutorials
  
  [“GitHub Training & Guides”](http://bit.ly/1KqBfC0) This is four part video tutorial from Github, each video is about 6 minutes.

  [“GitHub & Git Foundations”](http://bit.ly/2aXfzCu). It’s a 22 part video course on the basics of Github. Personally I couldn’t quite get into this course because of the video editing style but its worth having a look at as its made by Github themselves.

### Cheat Sheets
There are many cheat sheets on Git and here’s just a few of them. I’d recommend printing out at least one of these as your getting into Git and keep within arms reach. They are a very handy on a day to day basis. 

  * [“Git Cheat sheet” by Github](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)
  this is the one I use, it fits on a single sheet a paper double side printing
  
  * [“git - the simple guide - no deep shit”](http://rogerdudler.github.io/git-guide/)
  * [“Git Cheat sheet” by Tower](https://www.git-tower.com/blog/git-cheat-sheet/)

### Books
If your really keen and want to get the possibly best ebook on Git then the [Git Pro-git book](https://git-scm.com/book/en/v2) is what you want. Its not aimed at web dev newbies but you might want to be aware of it and at least peruse the introduction and contents pages to get an idea of how big Git is. However I’d suggest perhaps looking at this book after you’ve mastered the basics as it might be a bit too overwhelming for the newbie (its 364 pages long!).
The book is available for download in pdf, epub, mobi or html formats. 

#### Chapters include:
  * Getting Started
  * Git Basics
  * Git Branching
  * Git on the Server
  * Distributed Git
  * GitHub
  * Git Tools
  * Customizing Git
  * Git and Other Systems
  * Git Internals

### Podcast and Tutorials about Git Workflows
Once you've installed Git and mastered the basics then exactly how should your team employ Git? 
Tim Pettersen, a senior developer from Atlassian (the company that develops the Git GUI Sourcetree) has produced a [helpful tutorial on Git Workflows](https://www.atlassian.com/git/) as well as a [1 hour presentation](https://www.youtube.com/watch?v=O4SoB3TFkjA)  tip: If your short on time, skip the preamble and go to 8min 40s
The Git workflow is discussed again with Tim in episode 77 of “The Web Platform podcast” reviewed [“Project Management and Git Workflows”](http://thewebplatformpodcast.com/77-project-management-and-git-workflows). Indeed this podcast is well worth listening to generally.




## Part 3: A newbie guide to Git
I’ve suggested some courses and other resources it might be appropriate to present my own command line version of Git for newbies, aimed specifically at the “Im a newbie, just getting into web dev and I don’t know my bottom from my elbow” perspective. If that is you please read and let me know if I’ve been of any help, thats my aim. 

I can really only speak from my own learning perspective, hence constructive comments are welcome. I want illustrate Git how both from the command line perspective and, unlike the majority of online courses available as of August 2016, use a GUI Git specifically GitKraken. Frankly it’s a bit of an experiment so here goes!

I’ve decided to re-do nodeschool’s ‘Git-it’ course but this time adding the GitKraken GUI to mirror the same course topics.
 
To discuss how to use git, with the following (hopefully) memorable headings of:

  1) Github; a hub where pros show code
  
  2) To be hip, get Git
  
  3) git Github configured
  
  4) Command Line love
  
  5) GitKraken; a cracking way to see git
  
  6) To start your git, use intit !
  
  7) Whats your Status commander?
  
  8) Add your files to the Stage
  
  9) Don’t forgit, now Commit !
  
  10) What a diff rence a git makes
  
  11) Promote your Remote
  
  12) Clones and Forks: a perfect copy
  
  13) Your master Branch awaits
  
  14) Do Pull n Push
  
  15) The way of the git Master
  
  
  
## Github; a hub where pros show code

As with any other site, you need to enter your name, email address etc create a basic profile. Many coding sites use your Github account so make sure your details are correct.
You might want to watch this [a 40 second guide to signing up to Github](https://www.youtube.com/watch?v=ezxRcdJ8glM), made by Github.
Usually for a newbie to Github, the free unlimited public option is fine.



pic here



Click as appropriate or just skip



pic here



You need to verify your email address before continuing

Congratulations, if you've got to this screen you know have a Github account !
I’d suggest clicking the ‘Read the Guide’ If your new to Github, its a reasonably good guide. However if its a bit confusing don’t worry, it should make more sense as you interact with Github. 

Now we'll create our very first repository. 
Only if your creating a _brand new_ repository inside Github, thats doesn't exist anywhere else, then click the ‘Initialize this repository with a README’ otherwise don’t bother. In this case its brand new so its clicked.



pic here




Now we have our repository. If we click on the ‘clone or download’ button we can see the HTTPS URL link that we can use to connect this ‘remote’ to our local installation of Git on our machine. 



pic here



### Where to issue commands
You need to open up your terminal app (Mac / Linux), in windows this is called the Command Prompt 

   * Mac
  Open up your apps, then click on ‘other’ and select the terminal 

   * Linux
  Typically the keyboard shortcut is CTRL+ T  
  Alternatively it should be easily found in the menu;I suggest you keep your terminal on the desktop as e.g. a shortcut or on a dock.

   * [Windows](http://www.intowindows.com/command-prompt-as-administrator-in-windows-10/)


## To be hip, get Git
So you’ve created a Github account, but remember you still don’t necessary have Git on your local machine. The Git website provides detailed [instructions for installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git/) but hopefully the paragraphs below will make it easier for newbies.

Newbie Tip: don't actually type in the $ symbol, its just means normal user and visually shows where the where to type in the commands

#### Mac and Windows
The easiest way for Mac and Windows users is to [install Github Desktop](https://desktop.github.com) . This is a Git GUI from the company Github, but it will install Git onto your machine. We’re not using this particular Git GUI in the rest of the tutorial because its not available for Linux (rather bizarrely in my humble opinion).

Now open your terminal and enter

`$  git –-version`  (note the double hyphen i.e. -- )
    
You should see a version number higher than 1.7.10, in this case 2.7.4; 
now go to “GitKraken; a cracking way to see git”


see pic




#### Linux
First you’ll need to know your administrator password. Second we will make the perhaps grandiose assumption for the moment that typically Linux users who are newbies, are likely to be running a Debian or Ubuntu derivative.  

Use you desktop menu or shortcut key (try Ctrl+Alt+T)  to open up your terminal and type

`$  git --version`

if it returns a version number higher than 1.7.10 then skip to “GitKraken; a cracking way to see git”. Otherwise you need to install git by running the command

`$ sudo apt-get install git-all`

And for [other Linux distributions](https://git-scm.com/download/linux)



## Command Line love
You can change how your terminal looks, and how it shows off your git. For example it can be made to could look like this 



see pic


It has username, the git branch I’m on (more on this later) and the directory I’m currently in, but also they are different colours. 

It helpful and an optional extra. If you don’t want to do this right now then skip “to be hip, get Git”

Watch the video “Setting Up Your Workspace on Windows - How to Use Git and GitHub” from Udacity. There is a Mac/ Linux version and a Windows version.
Here’s a few details, but I’d recommend viewing the video and getting the resource notes from Udacity.


#### [Mac](https://www.youtube.com/watch?v=s_eFuGauy6k)
Open up a terminal and type  

`$ nano bash_profile`

this will open up your bash_profile nano , which is a basic text editor built into Linux and OSX.

Add the following to your profile 

`# Enable tab completion`

`source ~/git-completion.bash`

`# colors!`

`green="\[\033[0;32m\]"`

`blue="\[\033[0;34m\]"`

`purple="\[\033[0;35m\]"`

`reset="\[\033[0m\]"`

`# Change command prompt`

`source ~/git-prompt.sh`

`export GIT_PS1_SHOWDIRTYSTATE=1`

`# '\u' adds the name of the current user to the prompt`

`# '\$(__git_ps1)' adds git-related stuff`

`# '\W' adds the name of the current directory`

`export PS1="$purple\u$green\$(__git_ps1)$blue \W $ $reset"`

`alias brackets="open -a /Applications/Brackets.app"`


Note: The last line   
`alias brackets="open -a /Applications/Brackets.app"`


was because I use the [Brackets IDE](http://brackets.io) development tool.  If you use say [Atom](https://atom.io)  then you will have to change this line.

If you use [Sublime Text](https://www.sublimetext.com)  refer to [Ashley Nolan’s post](https://ashleynolan.co.uk/blog/launching-sublime-from-the-terminal) or [Udacity’s post](https://www.udacity.com/wiki/ud775/sublime) using ‘subl’

Save your bash_profile file; which in Nano is ‘CTRL’ + ‘O’ then exit ‘CTRL’ + ‘X’


#### Linux

First make your hidden files visible, this depends on what desktop you have. If its KDE your likley using Dolphin, so to show hidden files its ‘CTRL’  +  ‘ . ’. 
For other desktops its often ‘CTRL’ + ‘H’.  

the bash_profile file is typically located in the Unix System Resources directory (usr)   
`$ /home/user/.bash_profile`


#### Windows
Things are slightly different  different on Windows. You define how your IDE opens a different way for starters. Please see [Udacitiy’s excellent course for details](https://www.youtube.com/watch?v=IfLhXM4RnB4)

###Y our Global Git identity

Setting up your identity on Git is important. [From Git’s own handbook](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
The first thing you should do when you install Git is to set your user name and email address. This is important because every Git commit uses this information, and it’s immutably baked into the commits you start creating:

`$ git config --global user.name "John Doe"`

`$ git config --global user.email johndoe@example.com`

## GitKraken; a cracking way to see git



see pic



As of August 2016  GitKraken (the free versions) is available for Windows 7+, Mac OSX 10.8+ , Linux (specifically Ubuntu LTS 12.04+, Debian 8+, Fedora 21+), so many users should be covered.

For newbies,  just get the free version for now.

But If you become a happy GitKraken user then GitKraken pro costs $6/ month and gives you added features from the basic free version including: edit your merge conflict output in-app, multiple profiles for work & personal and email-based support.

You should now have a Github account, have Git installed on your local machine and also the GitKraken Git GUI installed.



## To start your git, use intit !
We discussed what Git is earlier what repositories are. But briefly a repository is a project folder or directory where your code is stored and also where the information about the flow of the contents contained in the folder are controlled and managed.

Lets make a directory called ‘CommunityTechLiverpool’ in the usual way you do on your machine. 
You can do this in the command line, or whatever way you normally do this


see pic


[ Note: I’ve deliberately set my Mac to show hidden files hence you can see a  ‘ .DS_Store file’   ignore this file, its just a Mac thing. ]
This is just a directory or folder. There is not Git version control attached to this directory.

To add Git to this directory, thus turning it into a repository or ‘repo’ we go through 2 steps
  * CHANGE into the right directory   `$cd`

  * INITIALISE git in this directory  `$ git init`

#### 1) CHANGE into the right directory  `$cd`

Now open up your terminal and type
`$ cd ~`     (to go change the directory ‘cd’ to the home ‘~’)

`$ ls  `    (to list the directories and folders in this directory)

now in my machine I want to go to a directory inside the Desktop so

`$ cd Desktop`

`$ ls` (ls means ‘list the directories and files’. You should see Desktop)

`$cd “Coding Training”`   (cd means ‘change directory’)

`$cd “Community Programming Projects”` 

`$cd CommunityTechLiverpool`   (no “ quotes ” as no spaces in the name)

`$ clear`   (this clears the terminal; but you can still scroll back up)

Alternatively on a Mac and some other OS’s, enter `$ cd` as before (don't’ forget a space after cd). Then visually drag the folder you want to change to in the ‘finder’ (or windows explorer) Hopefully this will automatically have generated the absolute directory path. Now hit enter as before.



see pic





#### 2) INITIALISE git in this directory  ($ git init)

`$ git init`
you should get a response with the words

`Initialized empty Git repository in …..`

like this




see pic




And if we now look in our directory using the standard Mac GUI we see a .git directory
This is where the actual git management and control resides.



see pic



But note the full stop or period. This indicates that its a hidden directory. I’ve enabled hidden directories just so we can see it.  If we go back to how we would normally see our files,  Git ‘disappears’.


see pic



## Whats your Status commander? 

Using the command line ($ git status) we can see where git is up to

`$ git status`
(which for a brand new repo should respond with the words )



see pic



So far so good, we’ve made a new git repo, checked its status. But theres nothing in it!
Lets put some files and a directory to our empty repo called ‘communityTechLiverpool”



see pic



if we `$ git status`



see pic


#### Whats happening?  Why isn’t git saving it?

If we read the status report it tells us that our files and folder aren't ‘staged’. There are three areas in Git that files pass through:


1) Working area

  This is the normal directory your files reside in.

  Git knows they are there but isn't monitoring them

2) Staging area

  You ‘add’ your files to Git. Now Git is monitoring your files but will tell you that you haven't committed them. 

  Your saying I have files, but they aren't ready yet  The code isn't at a logical point where it makes sense to commit to a change just yet. Say you were making a change in the CSS to make a button red colour. You wouldn’t want to commit the file when you've typed in “background: re ” . You’d want to put ‘red’ in. 

3) Repository

  Now final you do a commit. Now your satisfied that you've made a sensible logical change to the code. (e.g. “background: red”) 

  In this diagram we see that index.html and style.css have beed added to the staging area. They are being tracked by Git. But only index.html is committed. Style.css hasn’t yet reached a logical unit of change where it makes sense to commit the style.css code to the repository.




see pic



## Add your files to the Stage

We decide that it makes sence to add all our files to Git, so we 

`$ git add directory_name/`   (as is this case)

or

`$git add filename`       	(more typically)




see pic





Now Git has placed our directory with its contents into the staging area.

But we’ve still not finished, we need to commit!



## Don’t forgit, now Commit !
Suppose were satisfied that we’ve completed a logical change in the code in one or more of our files. In this case were happy that our images of musicians is acceptable for now.

`$ git commit -m “description goes here”`


see pic


Its normal to check that everything is ok so we git status again


see pic



Now we've made one commit, but normally there would be many more. To see this history, or log of commits its just 

`$ git log`


see pic


we see that there only a history of one commit at the moment. Recalling our files 


see pic



Now if we now change a file, lets say the index.html file and then save it 

`git status`



we see git has noticed the change, but exactly what has changed? Lets look at ‘diff’


## What a diff erence a git makes
If we recall our earlier picture of the different ares, working, stage and repository


see pic


Its sometimes useful to be able to see the differences between code thats in one area say the working area and the staged area.  For example:

`$ git diff `    shows the differences between working and staged areas



see pic



Another form of diff is when its used to compare the difference between two commits.
Taking our change above our index.html file is currently modified, put has not been added to the staging area.

Hence we 
`$ git add index.html`

then we will commit it
`$ git commit -m “added comment to demonstrate file change”`

so were good to go!  Now if we look at our commit history we should see 2 commits, the initial one when the files were created and the change we just made, lest check with `$ git log `



see pic







Indeed we have 2 commits !But whats the difference between those commits, the actual code differences?

`$ git diff [first commit number ] [second commit number] `




see pic





## Promote your Remote
Lets re-cap thus far we’ve 

  * Initialised a new Git repository
  * Understood that there are three areas for Git, working, staging and repository
  * added files to the staging area
  * Committed files to repository
  * changed a file and looked at the log of commits
  * looked at differences between working and staged areas
  * looked at the differences between two committed files 

phew!… 
However all our efforts have been on our local computer, the git that sits on our own machine.
What we really need to do is start file transfers between our local Git and our remote git, which typically is Github.



see pic



We want to PUSH files up to Github, and PULL files from Github
Now traditionally we call our main remote repository ‘origin’ and to add a connection from our local git to our remote Github, its just

`$ git remote add origin <Github URL goes here>`

Now open up the Github web page and go to the remote repo you want to connect to.
Then click on the ‘clone or download’ button and copy the URL.



see pic


So in this case its 
 
`$ git remote add origin https://github.com/commTechLiv/tutorials.git`

and to check what your remote is    `$ git remote –v`

and to PUSH files up to the remote  `$ git push <remote name> <branch name>`
 
`$ git push origin master`

or PULL files     `$ git pull <remote name> <branch name>`
 
`$ git pull origin master`

### Licensing
When you create a new repository for your project in GitHub you may include a software license. As a starting point, Github has created a website to help developers [choose a license](http://choosealicense.com)

### gitnore
You may want to ignore file. To do this use the .[gitnore file](https://git-scm.com/docs/gitignore) and [use gitnore for automated ignoring of typical files](https://www.gitignore.io) found in operation systems, [for example .DS_Store]( http://sourabhbajaj.com/mac-setup/Git/gitignore.html for example)

### Readme
This is a description of the project and perhaps how people can get involved or other useful information point for people interested in the project point of view, not simply a user.



## Clones and Forks: a perfect copy

Forking is when you create an exact copy, a ‘clone’ of a Github repository onto your Github repository. This clone is called a ‘fork’ in Github terminology and only exists on your Github account and just to be clear, ‘fork’ is a Github phrase, the generic term is ‘clone’.

Now to make this repository exist on your local machine you have to clone the Github       repository that you forked onto your local machine. It’s a clone of a clone. 



see pic



First check what remote your connected to	 `$ git remote -v`

You can always add another remote if you wish by 
`$ git remote add <name of remote>  <URL of remote>`

and if you have several remote repos, change the remote using
`$ git remote set-url <name of remote>  <URL of remote>`

Change your directory,  `$ cd..`  ,to where you want your cloned/ forked repo to be put locally.
Now clone the remote   `$ git clone <URL of remote repo>`

However its very likely that you’ll want to be able to refresh your locally cloned repo, pulling in the newer version thats on the remote repo. Rather than cloning the entire repo again, you can add the latest changes.

By convention the repo containing the latest changes is often called ‘upstream’. 
So to add this upstream remote

`$ git remote add upstream  <URL of remote repo ‘upstream’>`

## Your Master branch awaits
On of the main concepts in Git is branches. The illustration below shows commit’s being made along the main trunk of the project which called the ‘master’ branch .


see pic



Each member of the team has a clone of the master branch which they keep updated.

As they work on individual features these are developed as feature branches,. They only exist on the individual developers computer, no other developer can see the code. Once a developer is happy that the feature as reached a point where it can be reviewed then it may be cloned by a coder via a remote repo like Github.

Likewise  if the feature branch has reached a point where its to be considered ready to be merged with the main branch, the feature branch developer can make a request to the main branch project manager to pull the branch into the main branch and merge it in.

So to create a branch     `$ git branch <new branch name>`

and to switch to another branch   `$ git checkout <branch name>`

## Do Push n Pull
Getting branches to and from remote repos is called pushing and pulling

To pull in  the latest changes
`$ git pull <remote repo> <branch on repo>`

For instance if we wanted a branch were called  ‘development’  and say a remote called ‘upstream’  to be  pulled into your local repository
 
`$ git pull upstream development`

We can also push up changes, so if we want to push up a branch to say a remote called ‘origin’
`$ git push origin <branch name>`

####BUT, you might be refused….and this is  good thing!
This is an important concept called a ‘pull-request’
Proper project management ensures that code is not just taken ‘as is’ and is checked. Part of this checking is by other human codes . Thus a typical workflow is that when someone asks for code to be included in the main branch, a request to pull in their branch code is made.

Github makes this process easy , indeed ‘pull-requests’ are routine. Only where a team or project manager is happy (depending on how the git workflow is achieved) will code be accepted.

Indeed it might be accepted first into a development branch to be tested alongside other features to check for any inter-dependancies that may have been missed during the development of that feature  branch.

Only when the development branch is considered ‘stable’ will it be merged into the main ‘master’ branch, which is typically the branch that the customer or end-user sees.



see pic



Click on ‘pull-request’, and then changing the branch range and destination repository . Then click on the pull request button, enter a description and [create the pull-request](https://help.github.com/articles/creating-a-pull-request/)

Note that even though you may have forked your repo, and now ‘own’ that fork Github rembers its history, and you can alwsy do pull-requests back to the original repo. This is called [‘Creating a pull request from a fork’](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)

## The way of the git Master branch
Change to the branch you want to merge to	
`$ git checkout master`

To merge locally, 
`(master) $ git merge mydevbranch`


Now we've merged, we don’t need the old ‘mydevbranch’ branch so lets delete it using -d

`$git branch -d mydevbranch`



To merge a remote Github repository thats called ‘upstream’ and has a branch called ‘bob’
`$ git pull upstream bob`




## Git Workflows
The following is a summary of workflow approaches based of [Tim Pettersen’s 1 hour presentation](https://www.youtube.com/watch?v=O4SoB3TFkjA)  tip: If your short on time, skip the preamble and go to 8min 40s. Tim is a senior developer from Atlassian who make SourceTree and other software tools.

#### Basic ideas
  * Workflow is all about stability, traceability and isolating code under development.

  * If open-source, use forking, otherwise use branching.

  * The ‘best ‘ work flow depends on what the product is, the team structure and the impact of bugs for example.

  * Branch everything; feature branch, bugfix, ‘hotfix’ (a ‘live in the field’ bug) and a document change

#### Use a naming convention 
feature/ 	bugfix/ 		hotfix/  		doc/     
like bugfix/issue_number-description  e.g. bugfix/abcd1-dark-theme


#### Development branch
Consider the cases when features that whilst independently work fine, when merged to the main branch are buggy because they have dependancies between the new features.

Thus before releasing code to the main master branch (which is whats used in production and is what the customer sees), features are added to the development branch, which is the main branch the developers use. Once stable this branch is merged to the master branch.

#### Merge strategies
Typically the ‘merge commit’ is used, but also the ‘rebase (fast-forward)’

Rebasing is where the master branch has some features you want to merge into your developing feature branch but you don't want all the commits from many other coders that would be generated because they would complicate your own commit log on the feature branch your developing.

The ‘tip’ of the master is used to ‘rebase’ the merge instead; use with caution.

#### Use Pull-requests to instigate code reviews 
Use two coders to review code, don’t just use auto testing tools !

  * better code
  * team – shared knowledge
  * educates devs
  * team ownership of code


## Conclusion and Summary
Having covered the basics of Git and Github theres no excuse to use it when you next write code. In fact Github are looking at expanding the use of Git beyond just code [law, fonts, Gregorian chants] (https://github.com/CMAA/nova-organi-harmonia), but thats another story.

Now **git** coding ! 


## Resources

1.  [Git-scm](https://git-scm.com)
2.  [Pro-git: A superb free online book on Git](https://git-scm.com/book/en/v2)
3.  [Git-scm GUI Clients:](https://git-scm.com/download/gui/linux)
4.  [“10 Best Graphical Git Clients for Developers”:](http://www.freshtechtips.com/2015/03/git-client-windows-mac-linux.html)
5.  [Github Desktop:](https://desktop.github.com)
6.  [SourceTree](https://www.sourcetreeapp.com)
7.  [SmartGit](https://www.syntevo.com/smartgit/)
8.  [GitKraken](https://www.gitkraken.com/faq)
9.  [Git-Cola](http://git-cola.github.io)
10. [CodeSchool: “Git real”](http://gitreal.codeschool.com)
11. [Nodeschools: “Git-it”](https://github.com/jlord/git-it-electron)
12. [Udacity: “How to Use Git and GitHub ”](https://www.udacity.com/course/how-to-use-git-and-github--ud775)
13. [“GitHub for Noobs” by Travis Neilson](http://bit.ly/2buQQ9Z)
14. [“Git Video Tutorial” by Derek Banas](http://bit.ly/2aYkkyw)
15. [“GitHub Training and Guides”](http://bit.ly/1KqBfC0)
16. [“GitHub and Git Foundations”](http://bit.ly/2aXfzCu)
17. [Intland Software: Centralized vs Distributed Version](https://www.youtube.com/watch?v=_yQlKEq-Ueg)
18. [Tutorial on Git Workflows](https://www.atlassian.com/git/)
19. [Tim Pettersen Git Workflows](https://www.youtube.com/watch?v=O4SoB3TFkjA)
20. [Git Workflows: Episode 77 of “The Web Platform podcast” reviewed “Project Management and Git Workflows”](http://thewebplatformpodcast.com/77-project-management-and-git-workflows)