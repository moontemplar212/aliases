# aliases
GIT aliases

---

The list of git aliases that I use to help me write software and keep a good workflow.

Some useful ones are:

  > cmapnv = "!f() { git aa && git commit -a -m \"$1\" --no-verify && git push; }; f"

This one takes an argument, the commit message, and adds all the unstaged changes, commits them while skipping the verification process such as unit tests and others. Finally, the result is pushed upstream.

I find this useful as a one stop shop command that does it all. It takes your work and does all the steps required to merge them without having to type three separate commands. 

  >   parent = "!git log \"$1\"^ -1 #"

This one takes a commit number as an argument and shows the parent commit of that node. Pretty simple but sometimes you just really need to know this kind of thing.

  > pnb = "!git push -u origin \"$(git branch --show-current)\""

If you've ever created a new branch and wanted to push it in one go without having to type the branch name then this one's for you. Push New Branch inserts the current branch name as an arugment to the set-upstream shorthand flag -u. 

  > rhh = git reset HEAD^

While this one is not that complicated to understand; the power of it is truly amazing. Undoing bad commits doesn't have to be hard and with this it isn't. The HEAD^ is responsible for telling GIT to reset your branch to the state of HEAD ( the bad commit ) minus one commit, or the last good commit.

There are lots more included in the file so be sure to take a look.

Cheers,
moontemplar212.
