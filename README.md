



# Gerrit Usage



## What is _Gerrit_



![Procedures](https://github.com/sunyaojin/Gerrit/blob/master/fig/f4.png)



## How to use Gerrit


### Add SSH Key


+ Generate SSH key on your local machine 
    -   `ssh-keygen -t rsa`

+ Add SSH to Gerrit account

![add ssh key](https://github.com/sunyaojin/Gerrit/blob/master/fig/f1.png)

### Find the project you want to contribute

`Browse` -> `Repositories`

You can type the project name to find it. For example, type `NominisYS` to find `NominisYS/gerrit_demo`.

![find your project](https://github.com/sunyaojin/Gerrit/blob/master/fig/f3.png)



### Fork the project

Go to project page and copy `git clone ......`.

![fork project](https://github.com/sunyaojin/Gerrit/blob/master/fig/f2.png)






### Contribute code and commit




__Before commit to the changes, you need to add username and email info__

```bash
git config user.name test3
git config user.email test3@microwu.com
```




```bash
git add -A
git commit -a -m "add comment"
```






### Push to gerrit server

```bash
git push origin HEAD:refs/for/master
```

`refs/for/<target-branch>` 


## Terms


### Label `Verified`

```json
  [label "Verified"]
      function = MaxWithBlock
      value = -1 Fails
      value = 0 No score
      value = +1 Verified
      copyAllScoresIfNoCodeChange = true
```

It means that __compiles, passes basic unit tests__.







