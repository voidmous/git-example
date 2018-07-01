# Git Configuration

babun default `.gitconfig`:

```ini
[push]
	default = matching
[core]
	trustctime = false
	editor = vim
	filemode = false
[color]
	ui = true
[credential]
	helper = cache --timeout=3600
[merge]
	tool = vimdiff
[mergetool]
	keeptemporaries = false
	keepbackups = false
	prompt = false
	trustexitcode = false
[alias]
	last = log -1 --stat
	cp = cherry-pick
	co = checkout
	cl = clone
	ci = commit
	st = status -sb
	br = branch
	unstage = reset HEAD --
	dc = diff --cached
	lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative --all
[user]
	email = youremail
	name = yourname
```

## Cygwin WinMerge Integration

Best Solution: [Cygwin Git: wrappers for diffmerge and winmerge](https://gist.github.com/ecerulm/509918 ""), see comments for configuration before running.



Refer to : [windows - Is it possible to use winmerge to view git diffs from cygwin? - Stack Overflow](https://stackoverflow.com/questions/3780420/is-it-possible-to-use-winmerge-to-view-git-diffs-from-cygwin "")

# Debug Git

```shell
GIT_CURL_VERBOSE=1 GIT_TRACE=1 git pull origin master
```

More Details: [How can I debug git/git-shell related problems? - Stack Overflow](https://stackoverflow.com/questions/6178401/how-can-i-debug-git-git-shell-related-problems "")
