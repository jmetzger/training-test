# Using a subtree 

## Prerequisites - Existing local repo 

```
# in der bash 
cd .. 
cp -a training training-neu 
cd training-neu
```


## Walkthrough

```
git remote add -f training-git https://github.com/jmetzger/training-git.git
# weird, but needed 
git status 
git subtree add --prefix training training-git main --squash
```

## Updating 

```
git fetch training-git main
git subtree pull --prefix training training-git main --squash
```

## Push 

```
git subtree push --prefix=training training-git main
```


## Ref. 

  * https://www.atlassian.com/git/tutorials/git-subtree
