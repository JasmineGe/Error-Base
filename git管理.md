    git init
    git add .
    git commit -m "init app"
    git remote add origin https://github.com/JasmineGe/react-admin.git // 将本地与远程关联
    git push origin master // 推送到远程的 master
    git checkout -b dev // 本地生成 dev 分支
    git push origin dev // 将本地 dev 推送到远程
    git branch // 查看分支
    git checkout -b dev origin/dev  // 根据远程 dev 生成本地 dev
