---
layout: post
title: How to create a github repositories and must know commands to make your first commit
---
Hi everyone I know how confusing github seems at the bigning and every little comand seems to confuse you.

The Git environment is a vast and sometimes gets very complicated when you have to work on bigger projects. These days almost every software company use github as their first version controlling system.

Lets first konw what a repositry is.

<h3>So what is a repo</h3>
A directory or repo is a storage space where your projects can live. Sometimes GitHub users shorten this to “repo.” You can keep code files, text files, image files, you name it, inside a repository.

<h3>So now what is a commit</h3>
This is the command that gives Git its power. When you commit, you are taking a “snapshot” of your repository at that point in time,and finally push it to your repo this makes necessary updates inside your repo. Thus it helps store your projects and provide version controle power.

<h2>Fist Create a repo</h2>

<img src="https://raw.githack.com/KarandeepSinghCoder/blog/gh-pages/_posts/img/repo1.jpg" height="400px" width="700">
Make sure you inetilize it with a read me file.

<h2>Now its ready to be cloned in your pc</h2>

<img src="">
copy the clone repo url. Run cmd at the folder where you want to copy your repo, use <span style="font-weight: bold;">Git clone your-url</span> to start the clonning.
<img src="">

Now you have your Repo cloned at your pc.Make the necessary changes and then we will push it back again to the github repositry so as to reflect the changes made on pc in the repositry.

<h2>[git status]</h2>
Check if there are already some changes tracked in the repository by git? 
<span style="background-color: grey">git status</span> will list any files that are changed.
<img src=" ">

<h2>[git add .]</h2>
This is the first command that you'll run after making some changes to the project files.

The command analyzes all the repository files and adds all modified and new (untracked) files in the current directory and all subdirectories to the staging area, thus preparing them to be included in the next git commit which I'll explain in the next lines. Any files matching the patterns in the .gitignore file will be ignored by git add . 

<img src="">

<h2>[git commit -m "your commit message"]</h2>

git commit -m adds the changed files into a commit with a commit message as stated inside the inverted commas(in the hading). Using the option -m allows you to add and create a message for the commit in one command.
<p>The <code>m</code> flag is used for connecting a commit message to your commit for example `git commit -m "your message". <br>
</p>

<h2>[git push origin master]</h2>

You are ready to push your first commit to the remote repository. The push here is for pushing your changes which requires a branch to push to call it origin and then specify the branch name master (the default branch that always exists on any repository.

So git push origin master will take the local commit that you made in the above sections and upload it to the remote server on github for other people to collaborate.

<img src="">

<h2>Thus you have done making your first git commit</h2>
<h5>hopefully this bolg helped you. Thanks for reading.</h5>

