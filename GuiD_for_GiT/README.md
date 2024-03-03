# Git: The Coolest Thing Since Sliced Bread

Hey there, fellow code wrangler! So, you've decided to dive into the magical world of Git, huh? Well, buckle up because you're about to embark on a wild coding adventure!


## Chapter 1: Getting Started

Alright, listen up! First things first, you gotta summon Git into your coding lair. How, you ask? Easy peasy! Just initialize Git in your project folder like a wizard casting a spell.
```git init
```

### Un-Gitifying a Folder
Imagine you accidentally turned the wrong folder into a Git repository. Oopsie daisy! No worries, you can "un-gitify" it. Just follow these steps:
```$ cd <repository folder>  # Navigate to the folder
$ rm -rf .git  # Delete the hidden .git folder
```
Now, let's break down what's happening here:
- The -r flag (from "recursive") allows us to delete folders along with their contents.
- The -f flag (from "force") saves us from pesky prompts like, "Are you sure you want to delete this file? And this one? Oh, and this too?"
But hey, a word of caution: The .git folder stores your project's history. If you delete it, poof! Your project's history vanishes into thin air, with no chance of resurrection. Only the latest version of files will remain. So tread carefully, my friend!

###Checking Repository Status
Now, let's talk about keeping tabs on your repository's mood swings with the git status command (from the ancient texts of Git wisdom, "status" means "state" or "condition").
After initializing your repository, let's say "first-project," fire up the git status command. It'll tell you:
- The current branch you're on (e.g., "On branch master" or "On branch main").
- A gentle reminder that there are no commits yet (e.g., "No commits yet").
- A friendly nudge, indicating that to commit something, you first need to create it (e.g., "nothing to commit").
In simpler terms, it's like Git giving you a quick status update on how things are going. Handy, right?
Unlike git init, you'll find yourself using git status often. Whenever you're puzzled, just peek at your repository's status, and then decide what to do next.


## Chapter 2: Adding Files to the Repository

Alright, champ, so you've got your Git repository all set up and raring to go. But hey, what's a repository without any cool files in it? Let's fix that!

### Preparing Files for Safekeeping with git add
Picture this: You've got a brand new Git repository, but it's as empty as a library during a zombie apocalypse. Time to populate it with some juicy files!
So, let's say you've got two files in mind: todo.txt, where you'll jot down your to-dos, and readme.txt, where you'll spill the beans about your project.
Now, why text files, you ask? Well, because in the magical land of Git, any code is just a bunch of text. Whether you're slinging Python or scribbling YAML, it's all just ones and zeroes to Git!
So, fire up your command line and create those files in your project folder (let's call it first-project). Then, let's check the status:
```$ touch todo.txt
$ touch readme.txt # Files created: todo.txt and readme.txt
$ git status # Checking the status
```
Git's gonna tell you that these files are untracked, which basically means it hasn't started keeping an eye on them yet. Poor little fellas, lost in the vast coding wilderness!
Now, to the rescue comes git add. This nifty command prepares files for saving (or "committing" in Git lingo). And guess what? There's more than one way to skin a cat – or add files, in our case!
You can add files one by one:
```$ git add todo.txt
$ git add readme.txt
$ git status
```
Or, if you're feeling lazy efficient, you can add the whole darn folder:
```$ git add . # Adds the whole current folder
$ git status
```
And voila! The files marked in green are now officially tracked by Git and ready to be saved. But wait, we're not done yet!

### Understanding the Difference between Adding and Saving
Here's the scoop: git add is like tossing items into your shopping cart. It doesn't save anything yet – it just gets things ready for checkout. The real saving happens with a commit.
Think of it this way: adding files is like picking out items in an online store, and committing is like hitting that "Place Order" button.
So, remember, until you commit, your changes are just sitting there, waiting for you to hit that button and seal the deal.


## Chapter 3: Making Your First Commit

Alright, cowboy, it's time to take your Git game to the next level! Say hello to the mighty commit – the cornerstone of Git (and other version control systems).
A commit is like a time capsule for your code changes. It ensures that your changes are safely recorded in Git's history, ready to be revisited whenever you need to hit that magical "undo" button. Think of it as Ctrl+Z for your entire project – talk about power!

### Executing Your First Commit with 'git commit'
So, how do you make this mystical commit happen? Easy peasy! Just use the git commit command, along with the -m flag (short for "message") to attach a meaningful message to your commit.
Now, why do we need a message, you ask? Well, it's like leaving notes in the margins of a book – it helps others (and your future self) understand what the heck you were up to when you made those changes.
Let's dive right in and make our first commit. Navigate to your project folder (first-project) and unleash the power of Git with the following command:
```$ git commit -m 'My first commit!'
```
Hit Enter, and boom! Your current files are now immortalized in Git's history with the message "My first commit!" attached. It's like taking a snapshot of your project at this exact moment in time.

### Understanding the Commit Message
But wait, there's more! Git is gonna throw some info your way after you commit. Here's what it means:
- [master (root-commit) baa3b6e]: This tells you that the commit was made in the master branch and that it's the root commit (the very first one) in this branch. baa3b6e is a unique identifier for this commit, but more on that later.
- 2 files changed, 1 insertion(+): Aha! Your commit affected two files (readme.txt and todo.txt), and you made one insertion (added one line).

### A Word on 'git add' vs 'git commit'
Remember how we talked about git add being like gathering your friends for a photo shoot? Well, git commit is like actually taking the photo. First, you prep your files with git add, and then you seal the deal with git commit.
To drive the point home, let's use another analogy: Say adding files is like getting your friends in position for a photo, and committing is like snapping the picture. The resulting photo is your commit – frozen in time, forever immortalized in Git's history.
Oh, and by the way, "My first commit!" might not be the most informative commit message. You'll want to describe your changes in a way that's crystal clear, like "Added crucial task to TODO" or "Fixed bug in loop."


## Chapter 4: Peeking into Commit History

Welcome to the history class of your Git journey! In this lesson, we'll learn how to dig into the treasure trove of commit history, an essential skill for tracking the evolution of your repository.

### Viewing Commit History with 'git log'
Remember those commits you made in the previous lesson? Well, it's time to unleash the power of git log to see them in all their glory! Just type git log into your command line, and prepare to be amazed.
By default, git log spits out commits in reverse chronological order – meaning the latest commits appear at the top. You can confirm this by checking the creation date and time of each commit.
If you run git log and find only one commit or none at all, don't panic! Just take a deep breath, go back to the previous lesson, and double-check that you followed the right sequence of git add and git commit.
And there you have it – a window into the past, showcasing the journey of your project through time.


## Chapter 5: Getting to Know GitHub

Up until now, you've been rocking Git solo – your project first-project has been chilling only on your computer. But here's the kicker: one of Git's coolest perks is its ability to facilitate teamwork. To share your repository – say, with your pals – you need to give it a new home in the cloud.

### What Exactly is GitHub?
GitHub is more than just a place to dump your code – it's a bustling marketplace of ideas and collaboration, all powered by Git. Think of it as your one-stop shop for sharing, exploring, and building cool stuff with other folks.
The name "GitHub" comes from the English word "hub," which means a central station. And boy, is GitHub central! It's the go-to platform for storing Git repositories, used by big names like Google, Apple, and Valve for their projects.

###Why GitHub Rocks
GitHub isn't just a platform – it's a community. Whether you're sharpening your Git skills, collaborating with your team, or diving into open-source projects, GitHub has got your back. You can create projects of different flavors:
- Private – just for your eyes.
- Team-based – exclusive to your squad.
- Public – open for all to see.
And here's the cherry on top: you can hop on board someone else's open-source project and join forces with developers from all corners of the globe.

### Signing Up for GitHub
1. In the top right corner of the GitHub homepage, click on "Sign up."
2. You'll be prompted to enter the following details:
    2.1. Enter your email address.
    2.2. Create a password.
    2.3. Choose a username.
3. GitHub will ask if you want to receive product updates and announcements via email. Type "y" for yes or "n" for no.
4. Click on "Continue."
5. Complete the captcha challenge presented by GitHub.
6. After successfully completing the captcha, click on "Create account."
7. Enter the short code sent to your email address for verification purposes.
Congratulations! You've successfully registered on GitHub, the largest web hosting platform for projects. Now you have the opportunity to collaborate with millions of professionals worldwide, exchange ideas, and grow as a developer.


## Chapter 6: Creating a Remote Repository

###Step-by-Step Guide to Creating a Repository on GitHub
1. Navigate to your profile by following this link: https://github.com/username, where "username" is the name you provided during registration.
2. This page acts as your showcase, displaying you and your projects. If you see the message "You don't have any public repositories yet," it means you haven't created any projects.
3. Create a new repository by clicking on the "Repositories" tab, then hit the green "New" button on the right.
4. A window for creating a new repository will appear. Name it "first-project." While the name of the remote repository doesn't necessarily have to match the name of the project folder on your computer, for clarity, let's keep them consistent.
5. You can leave the other fields blank for now. Click confidently on the green "Create repository" button at the bottom.
6. Voila! Your remote repository is created, and its page will open automatically.
Now, all that's left is to link the remote repository to your existing local one on your computer. GitHub provides instructions for this under the section "...or push an existing repository from the command line."


## Chapter 7: Getting to Know SSH. Let's Generate SSH Keys, Shall We?

Picture this: you've got a key to a door behind which lies an important document. To access this document, you need to insert the key into the lock and give it a twist. Since only you have the key, your document is safely guarded from prying eyes.
Similarly, to access a repository on GitHub, you need to provide a key that confirms your identity and rights to read or modify data. Without this key, access is restricted. Let's delve into this in our lesson, shall we?

### What's SSH Anyway?
When computers exchange data over a network, they follow network protocols — rules for exchanging data between computers. One of the most common network protocols is SSH (Secure Shell Protocol). It ensures secure data exchange over a network. Using this protocol, you can fetch data from or send it to a remote computer. The traffic is encrypted, making the protocol secure.
SSH employs a pair of keys to ensure security — the public and private keys:
- The private key is stored only on your computer and should not be shared with anyone else. It's used for decrypting data.
- The public key is available to everyone and is used for encrypting data. It can be decrypted by its corresponding private key.
Only you can decrypt data using the private key, but anyone possessing the public key can encrypt data for you. These two keys are linked and form an SSH pair. You'll likely use them in the future to interact with GitHub and other remote servers.

### Checking for the Existence of SSH Keys
Before generating SSH keys, make sure you don't already have them. By default, the directory containing SSH keys is in the user's home directory. Navigate there.
```$ cd ~ # navigate to the home directory
```
Usually, SSH keys are located in the .ssh/ directory. You can check for the existence of this directory and its files using the following command.
```$ ls -la .ssh/ # list any created keys
```
If the folder is empty or doesn't exist, you're good to go. If there are files with similar names, SSH keys have already been created:
- id_dsa.pub;
- id_ecdsa.pub;
- id_ed25519.pub;
- id_rsa.pub.
If you haven't created these files yourself, delete them.

### Instructions for Generating SSH Keys
To generate an SSH pair, you can use the ssh-keygen program. Open the terminal and enter the following command.
```$ ssh-keygen -t ed25519 -C "your_email@example.com" 
```
Use the email associated with your GitHub account. If you encounter an error message, your system likely doesn't support the ed25519 encryption algorithm. No worries, use another algorithm.
```$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com" 
```
After entering this command, you'll see the following message.
```> Generating public/private rsa key pair. # a public and private key pair has been generated
```
Specify where to store the keys. The default is the user's home directory. Press Enter to accept the default location.
```macOS
> Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter] 
Windows
> Enter a file in which to save the key (C:\Users\<username>\.ssh\):[Press enter] 
```
Now, a pair of keys will be created in the specified directory.
The program will prompt you for a passphrase to access the SSH key. You can leave it empty. Press Enter, then Enter again to confirm.
```> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again] 
```

### To Be or Not to Be a Passphrase
Oddly enough, a passphrase is like a "key to the key." Imagine your SSH key is in a box. On the box itself, there's a combination lock that opens with a passphrase.
Many Git users don't use a passphrase to protect their SSH keys. If there's no passphrase, you don't need to enter it each time you interact with a remote repository.
On the flip side, using a passphrase enhances key security. If you do use one, your key will be securely protected if your computer is accessed without authorization.
All set! Now, let's check if the keys were indeed generated. Run this command.
```ls -a ~/.ssh 
```
You should see two files — one with a .pub extension and one without. The .pub file is public, meaning you can share it with websites or colleagues. The file without the .pub extension is private. Never share it with anyone! 🗝️


## Chapter 8: Linking Your SSH Key to GitHub

In the previous lesson, you generated an SSH key, but it's not yet linked to your GitHub account. Let's fix that, shall we?

###Instructions for Linking Your SSH Key and GitHub Account
After running the ssh-keygen command from the previous lesson, two files will be created in the ~/.ssh directory — id_ed25519 and id_ed25519.pub (or id_rsa and id_rsa.pub depending on the algorithm you used):
- id_ed25519/id_rsa — the private key (the file without .pub at the end). Never copy or share it with anyone.
- id_ed25519.pub/id_rsa.pub — the public key (indicated by the .pub extension).

### Copying the Public Key to GitHub
*MacOS*
```# Copy the contents of the key to the clipboard:
$ pbcopy < ~/.ssh/id_rsa.pub  # For ed25519 use the next command:
$ pbcopy < ~/.ssh/id_ed25519.pub 
```
Here, the pbcopy command is used to copy the data stream to the clipboard. The command pbcopy < ~/.ssh/id_rsa.pub means "Copy the entire contents of the ~/.ssh/id_rsa.pub file to the clipboard." Alternatively, you can print the file to the screen using cat ~/.ssh/id_rsa.pub and manually copy it.
*Windows* 
``` # Copy the contents of the key to the clipboard:
$ clip < ~/.ssh/id_rsa.pub
# For ed25519:
$ clip < ~/.ssh/id_ed25519.pub 
```
If clip doesn't work, display the contents of the file using cat ~/.ssh/id_rsa.pub or cat ~/.ssh/id_ed25519.pub and copy the output from the console to the clipboard.

### Linking on GitHub
1. Navigate to GitHub and select "Settings" from the account menu.
2. In the left menu, click on "SSH and GPG keys."
3. On the opened tab, select "New SSH key."
4. In the "Title" field, write the name of the key, e.g., "Personal Key."
5. The "Key type" should be "Authentication Key."
6. In the "Key" field, paste your key from the clipboard.
7. Click on the "Add SSH key" button.

### Verifying the Key
Check the correctness of the key using the following command.
```$ ssh -T git@github.com 
```
If this is your first time using Git to share a project on GitHub, you'll see a similar warning.
```The authenticity of host 'github.com (140.82.121.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU. 
This key is not known by any other names. 
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
This warning indicates that you've never connected to the GitHub server before. Therefore, Git can't guarantee that the server is who it claims to be.
To confirm authenticity, the server generates and publishes SHA256 keys. You can check the GitHub keys at this link. If the key in the warning matches what you see on the site, the server is valid. Type "yes" to continue. You'll see a welcome message on the screen.
```Hi %YOUR_ACCOUNT%! You've successfully authenticated, but GitHub does not provide shell access.
```
Congratulations! Your SSH key is now linked to your GitHub account, opening up a world of collaboration possibilities.


## Chapter 9: Linking Your Local and Remote Repositories

You now have a local repository named first-project, stored on your computer, and a remote repository on GitHub. You've generated an SSH key for secure operations and are ready to link the remote repository with the local one.

### Linking the Remote Repository to the Local One with git remote add
1. Go to the page of your remote repository, choose the SSH option, and copy the URL. A button on the right will allow you to do this instantly.
2. Open the console, navigate to the directory of your local repository, and enter the git remote add command.
```$ cd ~/dev/first-project
$ git remote add origin git@github.com:%YOUR_ACCOUNT%/first-project.git
```
The command needs two parameters: the name of the remote repository and its URL. Use the word origin as the name, and paste the URL you copied from the remote repository page.

### Verify that the Repositories are Linked with 'git remote -v'
Great! You've linked the local repository with the remote one. Now, let's make sure everything is working with the following command.
```$ git remote -v
```
In the output, you should see two lines similar to those shown below:
```origin    git@github.com:%YOUR_ACCOUNT%/%PROJECT-NAME%.git (fetch)
origin    git@github.com:%YOUR_ACCOUNT%/%PROJECT-NAME%.git (push)
```
The -v flag is the short form of the --verbose flag, which displays more information in the output.


## Chapter 10: Synchronizing Your Local and Remote Repositories

Now, let's talk about flinging your changes into the digital abyss. But first, a crash course on branches, because why not?

### Main Branch: The Big Cheese
Imagine branches as funky parallel universes where your code parties. Each commit is like a snapshot of your code's shenanigans frozen in time. The main branch is like the OG universe, where all the cool kids hang out. It used to be called master, but then GitHub decided to give it a makeover and named it main. Because why stick to one name, right?

### Wham, Bam, Thank You git push!
So, you've done the commit cha-cha - staged your files with git add and committed them with git commit -m. Now, it's time to hit the turbo boost and fling those code nuggets to GitHub's cosmic cloud using the almighty git push command.
The first time around, toss in the -u flag along with origin (your remote repo's nickname) and main or master (your current branch's name) like so:
```$ git push -u origin main # If this gives you grief, try 'master' instead of 'main'.
```
It's like telling your code, "Fly, my pretties, and show the world what you're made of!"

###Playing in GitHub's Digital Sandbox
GitHub's playground is where the real fun begins. Click that "commit" button and watch your code come to life. You can even click on commit messages to see what mischief your code's been up to. It's like a virtual circus for your code monkeys!

###Your Quest, Should You Choose to Accept It
1. Open your project on GitHub and summon a file called task.txt using touch.
2. Sprinkle some magic into task.txt - add some jokes, unleash your creativity, you do you.
3. Commit your changes and blast them off to the GitHub mothership using git push.
```$ git push
```
4. Use the GitHub interface to bask in the glory of your latest commit. Click on the commit message and let the applause roll in.


## Chapter 11: README.md: The Epic Saga of Your Project

Hey there, fellow code wranglers! So, you wanna tell the world what your project's all about, right? Enter the README.md file - your digital business card, your project's hype man, your ticket to fame and fortune (okay, maybe not the last one).

### What's the Scoop?
So, what should you cram into this digital dossier? Well, here's the lowdown:
1.  Project Title and Elevator Pitch: Give it a snazzy name and a quick rundown of what it's all about. Who made it, why it exists, what problems it solves - you know, the usual chit-chat.
2. Tech Specs: What kind of wizardry powers this project? Spill the beans on the tech stack and why yours is cooler than all the rest.
3. User Manual: No IKEA-style assembly required here. Just a handy guide on how to use your creation - think of it as your project's GPS for lost souls.
4. Future Plans: Got big dreams? Lay 'em out here. World domination? Maybe. Cat video integration? Why not?

### Formatting Shenanigans
Now, let's talk Markdown. It's like HTML's cooler, more laid-back cousin. Here's a crash course:
- Headers: Think of them as the big, flashy billboards of your README world. Pound signs all the way down from H1 to H6. 
p.s. use #s (the less of their amount the bigger text)
- Paragraphs and Line Breaks: Wanna start a new paragraph? Double-tap that Enter key. Need a line break? Two spaces at the end of a line or <br> if you're feeling fancy.
- Text Styling: Italicize with asterisks(*bla*) or underscores (_bla_), bold with double asterisks(**bla**) or double underscores(__bla__), and strike through with tildes(~~bla~~). Get wild, my friend.
- Lists: Numbered or bulleted, take your pick. Just remember - it's all about the presentation.
- Links: Got a URL to flaunt? Wrap it in square brackets and drop it in some round ones. Add a title for extra flair.
- Code Blocks: Highlight your code snippets with triple backticks. Bonus points for specifying the language.

**Have a great time, and ride easy, Git!
With your README, you're sure to be a hit!**
