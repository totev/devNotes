
# prettier and information rich log
git config --global alias.ls 'log --stat --pretty --graph'

# Folder based git configurations:

Add to ~/.gitconfig 

`
[includeIf "gitdir:~/dev/proj/"]
	path = ~/.gitconfig-work
`
