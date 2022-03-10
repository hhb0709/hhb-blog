##### 查看所有远程分支
```
git branch -r
```

##### 查看本地分支与远程分支的映射关系
```
git branch -vv
```

[Git Branch Upstream](https://blog.csdn.net/tterminator/article/details/78108550)

#####  git拉取远程分支并创建本地分支
```
git checkout -b 本地分支名  origin/远程分支名x
```

##### git设置代理
```
git config --global http.proxy 'socks5://127.0.0.1:1080'

git config --global https.proxy 'socks5://127.0.0.1:1080'

# 取消
git config --global --unset http.proxy

git config --global --unset https.proxy
```