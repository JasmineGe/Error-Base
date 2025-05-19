    git init
    git add .
    git commit -m "init app"
### 将本地与远程关联
    git remote add origin https://github.com/JasmineGe/react-admin.git
### 推送到远程的 master
    git push origin master 
### 本地生成 dev 分支
    git checkout -b dev 
### 将本地 dev 推送到远程
    git push origin dev 
### 查看分支
    git branch 
### 根据远程 dev 生成本地 dev
    git checkout -b dev origin/dev 
### 从远程 dev 拉取到本地 dev
    git pull origin dev 
