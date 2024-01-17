## souread 源码阅读分析

打印所有 commit 记录到 note.md 方便记录与查看
```
git log --reverse --pretty=format:"## %h %s" > note.md
```

几个方便跳转记录的脚本，分别命名为各命令的名字。
```sh
#!/bin/sh

first() {
	branch=`git symbolic-ref refs/remotes/origin/HEAD`
	git log --reverse --pretty=%H $branch | head -1 | xargs git checkout 
}
first "$@"

last() {
	branch=`git symbolic-ref refs/remotes/origin/HEAD`
	git log --pretty=%H $branch | head -1 | xargs git checkout 
}
last "$@"

prev() {
	branch=`git symbolic-ref refs/remotes/origin/HEAD`
	if [ -z "$1" ]; then
		n=1
	else
		n=$1
	fi
	git checkout HEAD~$n 
}
prev "$@"

next() {
	branch=`git symbolic-ref refs/remotes/origin/HEAD`
	if [ -z "$1" ]; then
		n=1
	else
		n=$1
	fi
	git log --reverse --pretty=%H $branch | grep -A $n $(git rev-parse HEAD) | tail -1 | xargs git checkout
}
next "$@"
```
