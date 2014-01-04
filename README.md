git-experiments
===============

Using this repository as a playground to understand how to resolve botched merged as well as its implications

Strategy
========
- Commit a few things to master
- Create a branch
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
