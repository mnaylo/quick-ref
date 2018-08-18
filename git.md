## Setting Your Identity 
The first thing you should do when you install Git is to set your user name and email address. This is important because every Git commit uses this information, and it’s immutably baked into the commits you start creating:

  * $ git config --global user.name "John Doe"
  * $ git config --global user.email johndoe@example.com
  

## Setting Your Editor
Now that your identity is set up, you can configure the default text editor that will be used when Git needs you to type in a message. If not configured, Git uses your system’s default editor. If you want to use a different text editor, such as nano, you can do the following:

  * $ git config --global core.editor "nano"

## Checking Your Settings
If you want to check your configuration settings, you can do the following:

  * $ git config --list 
  

## Initializing a Repository in an Existing Directory
If you have a project directory that is currently not under version control and you want to start controlling it with Git, you first need to navigate to that project’s directory. Once there, you can do the following:

  * $ git init 
  

## Cloning an Existing Repository
If you want to get a local copy of an existing Git repository, use git clone <url>. For example, if you want to clone the Git linkable library called libgit2, you can do so like this:
  $ git clone https://github.com/libgit2/libgit2
That creates a directory named libgit2, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new libgit2 directory that was just created, you’ll see the project files in there, ready to be worked on or used.
If you want to clone the repository into a directory named something other than libgit2, you can specify that as the next command-line option:

  * $ git clone https://github.com/libgit2/libgit2 mylibgit

*That command does the same thing as the previous one, but the target directory is called mylibgit.*


## Recording Changes to the Repository
At this point, you should have a bona fide Git repository on your local machine, and a checkout or working copy of all of its files in front of you. Typically, you’ll want to start making changes and committing snapshots of those changes into your repository each time the project reaches a state you want to record.
Remember that each file in your working directory can be in one of two states: tracked or untracked. Tracked files are files that were in the last snapshot; they can be unmodified, modified, or staged. In short, tracked files are files that Git knows about.

Untracked files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area. When you first clone a repository, all of your files will be tracked and unmodified because Git just checked them out and you haven’t edited anything.
As you edit files, Git sees them as modified, because you’ve changed them since your last commit. As you work, you selectively stage these modified files and then commit all those staged changes, and the cycle repeats.


## Checking the Status of Your Files
The main tool you use to determine which files are in which state is the git status command. If you run this command directly after a clone, you should see something like this:

  * $ git status

  On branch master
  Your branch is up-to-date with 'origin/master'.
  nothing to commit, working directory clean

*This means you have a clean working directory — in other words, none of your tracked files are modified. Git also doesn’t see any untracked files, or they would be listed here.*


## Tracking New Files
In order to begin tracking a new file, you use the command git add. To begin tracking the README file, you can run this:

  * $ git add README

*If you run your status command again, you can see that your README file is now tracked and staged to be committed:*


## Committing Your Changes
Now that your staging area is set up the way you want it, you can commit your changes. Remember that anything that is still unstaged — any files you have created or modified that you haven’t run git add on since you edited them — won’t go into this commit. They will stay as modified files on your disk. In this case, let’s say that the last time you ran git status, you saw that everything was staged, so you’re ready to commit your changes. The simplest way to commit is to type git commit: 

  * $ git commit
  

## Pushing to Your Remotes
When you have your project at a point that you want to share, you have to push it upstream. The command for this is simple: git push <remote> <branch>. If you want to push your master branch to your origin server (again, cloning generally sets up both of those names for you automatically), then you can run this to push any commits you’ve done back up to the server:

  * $ git push origin master

*This command works only if you cloned from a server to which you have write access and if nobody has pushed in the meantime. If you and someone else clone at the same time and they push upstream and then you push upstream, your push will rightly be rejected. You’ll have to fetch their work first and incorporate it into yours before you’ll be allowed to push.* 



###### For full documentation, see: https://git-scm.com/book/en/v2

