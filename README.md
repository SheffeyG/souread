## souread

format print the commits as the note:
```
git log --reverse --pretty=format:"## %h %s" > note.md
```

use scripts to quick checkout commits
```sh
chmod +x tools/
mv tools/* /usr/bin
```
