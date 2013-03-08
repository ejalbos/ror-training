Things for making git easier to use:

- Aliases:
Add the following to your ~/.gitconfig file

[alias]
        st = status
        co = checkout
        ci = commit
        br = branch
        alias = config --get-regexp 'alias.*'
        amend = commit --amend
        lg = log --graph --pretty=format:'%Cred%h%Creset -%C(bold yellow)%d%Creset %s %C(bold green)(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
        wip = commit -am'wip'
        rmt = remote

Now you can do 'git ci' instead of 'git commit', etc.

- Command line prompt:
Put this in your .bashrc somewhere:

```
PS1='[\u@\h \W$(__git_ps1 " (%s)")]\$ '
```

Then you can have the branch and mod indicators on your prompt line:

```
[ejalbos@vbox-ubuntu siq-ror-training (master)]$
```

It may need something else to run, but I didn't find anything obvious. Again, YMMV.