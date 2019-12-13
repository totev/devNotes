
### prettier and information rich log
git config --global alias.ls 'log --stat --pretty --graph'

### Folder based git configurations:

Add to ~/.gitconfig 

`
[includeIf "gitdir:~/dev/proj/"]
	path = ~/.gitconfig-work
`

### Rewrite committed and not yet pushed commit message
	git commit --amend -m "New message"

This also works with adding files, just do ```git add -A``` before ammend.