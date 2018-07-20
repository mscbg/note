from network

github fork一个分之后，过一段时间就会和主分支的差异比较大。 这样提交pr的时候就会冲突，这个时候我们就需要和主分支同步代码。

步骤：

1. git remote add upstream git@github.com:coreos/etcd.git   //本地添加远程主分支，叫upstream。可以先git branch -v查看是否已添加远程分支，若已添加，该步骤略过。

2. git fetch upstream  // 获取主分支的最新修改到本地；

3. git merge upstream/master  // 将upstream分支修改内容merge到本地个人分支；

    // 该步骤或者可以分成2步：

    1） # git checkout master；  // checkout到master分支

    2） # git merge upstream；  //合并主分支修改到本地master分支；

4. git push                                // 将本地修改提交到github上的个人分支
