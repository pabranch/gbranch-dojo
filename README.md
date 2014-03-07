# Git Branching Katas

Hands on Git branch manipulation.
> "you are in a maze of twisty little passages, all alike"---Colossal Cave Adventure

------------------------------------------------------------------
## Apply Changes
```
git checkout DEST

git merge SRC
OR
git merge --squash SRC
OR
git cherry-pick SRC
```
```
git checkout SRC

git rebase DEST
```

Technique | HEAD | local | remote | Parents |
-|-|:-:| 
merge | DEST | DEST | SRC | 2
merge --squash | DEST | DEST | SRC | 1
cherry-pick | DEST | DEST | SRC | 1
rebase | SRC | DEST | SRC | 1

## Rebase

Starting after the common ancestor:

    git rebase DEST [SRC]

Start after specified commit:

    git rebase --onto DEST START [SRC]

should be

    git rebase DEST --start=START [SRC]


## Deliver Completed Work

## Glossary
<dl>
  <dt>SRC</dt>
  <dd>Source: The commit(s) to apply; "theirs"</dd>
  <dt>DEST</dt>
  <dd>Destination: Resulting commit(s); "ours"</dd>
  <dt>Ancestor</dt>
  <dd>Past commit reachable from HEAD</dd>
  <dt>Descendant</dt>
  <dd>Future commit that contains HEAD</dd>
  <dt>Common Ancestor</dt>
  <dd>Past commit reachable from both SRC and DEST</dd>
</dl>

## Stuff to include
__ahead 1, behind 2__
__Fast Forward__

    git configure branch.master.options ff-only

## Workspaces:

### origin    remote repo

### user-A-ws	Abel
    git config user.name Abel

### user-B-ws	Betty
    git config user.name Betty

### user-C-ws	Chris
    git config user.name Chris

## Branches:
### master
### sprintX/patch-dev-complete
### sprintX/minor-dev-complete
### sprintX/major-dev-complete

## Tags

### test/patch
### test/minor
### test/major

## Ad-hoc Branches

### urgent
### db-only