git-experiments
===============

Using this repository as a playground to understand how to resolve botched merged as well as its implications

Strategy
========
- Commit a few things to master
- Create a feature branch
- Commit more to master
- Commit more to branch
- Merge master into branch, intentionally sabatoge a conflict
- Commit more to branch
- Undo
- Resync branch with master

Strategies to Resolve Borked Merge
==================================
1. Peel back commits via 'git revert' and re-apply
2. Revert-revert the merge
3. Rebase and change branch remote history

Commands
========
Commit a few things to master:
```bash
touch foo
git add foo
git commit -m 'Foo!'
touch bar
git add bar
git commit -m 'Bar!'
git push -u origin master
```

Create a feature branch:
```bash
git checkout -b feature
git push -u origin feature
```

Commit more to master:
```bash
echo 'This is some other content' > baz
git add baz
git commit -m 'Baz!'
git push -u origin master
```

Commit more to feature branch:
```bash
echo bazzzzzzz > baz
git commit -m 'Baz!'
git push -u origin feature
```

Merge master into feature branch and sabatoge:
```bash
git merge master
git mergetool # resolve & botch conflict
git commit
```

Commit more to branch:
```bash
touch quux
git add quux
git commit -m 'Quux!'
git push -u origin feature
```
