# all-repos
```
git remote add parser-remote git@github.com:aswinthomas/xml_parser.git
git subtree add --prefix=xml_parser/ parser-remote master
```
Now you can see commits from all repos in one place

Make changes in all-repos repo as you normally would i.e. git add -A, git commit -m "", git push origin master, then to sync back the changes,
```
git subtree push --prefix=xml_parser parser-remote update-build
```
This creates a branch in xml_parser with branch update-build that has the new changes. You can open a pull request and merge into master.

If you made changes in xml_parser, and if you need to sync back the updates, you have to do the following here
```
git subtree pull --prefix=xml_parser --squash parser-remote master
```
