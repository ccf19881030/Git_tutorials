# [How do I delete a local branch in Git?](https://www.git-tower.com/learn/git/faq/delete-local-branch)
Git makes managing branches really easy - and deleting local branches is no exception:
```
$ git branch -d <local-branch>
```

In some cases, Git might refuse to delete your local branch: when it contains commits that haven't been merged into any other local branches or pushed to a remote repository.
This is a very sensible rule that protects you from inadvertently losing commit data.

If you want to delete such a branch nonetheless (e.g. because you've programmed yourself into a dead end and produced commits that aren't worth keeping) you can do so with the "-D" flag:
```
$ git branch -D <local-branch>
```

This will force deletion of the branch, even if it contains unmerged / unpushed commits. It goes without saying: please be careful with this command!

# Can I undo deleting a branch?
In most cases, if you don't let too much time pass, you can restore a deleted branch.

If you're working with Git on the Command Line, you should take a look at a Git tool called "Reflog". 
Learn more about this in our free [First Aid Kit for Git](https://www.git-tower.com/learn/git/first-aid-kit) video series.

If you're using the [Tower Git client](https://www.git-tower.com/?utm_source=learn-website&utm_campaign=git-faq&utm_medium=easy-in-tower&utm_content=delete-local-branch), you can simply press CMD+Z (or CTRL+Z on Windows) - like you would to undo changes in a text editor - to undo the deletion and restore the branch:

You can undo many other Git operations with this familiar keyboard shortcut. 
[Have a look at everything that Tower allows you to undo!](https://www.git-tower.com/features/undo/)

# How do I delete a remote branch in Git?
To delete a remote branch, you need to use the "git push" command:
```
$ git push origin --delete <remote-branch-name>
```

# Learn More
- Check out the chapter [Branching can Change Your Life](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/branching-merging/branching-can-change-your-life) in our free online book
- More [frequently asked questions](https://www.git-tower.com/learn/git/faq) about Git & version control

