# Learn Git

### [常用 Git 命令清单](https://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
![关系图](https://www.ruanyifeng.com/blogimg/asset/2015/bg2015120901.png "关系图")
* Workspace：工作区
* Index / Stage：暂存区
* Repository：仓库区（或本地仓库）
* Remote：远程仓库
1. 新建代码库
2. 配置
3. 增加/删除文件
4. 代码提交
5. 分支
6. 标签
7. 查看信息
8. 远程同步
9. 撤销
10. 其他
## 极客时间-Git课程内容
### Git 基础
* https://git-scm.com/ 官网安装git
* 添加最小配置
    * 配置User信息
        ```
        git config [--local | --global | --system] user.name 'Your name'
        git config [--local | --global | --system] user.email 'Your email'
        ```
    * 查看配置
        ```
        git config --list [--local | --global | --system]
        ```
        local：区域为本仓库，只有在.git文件内才能配置，优先级最高
        global: 当前用户的所有仓库
        system: 本系统的所有用户
* 建 Git 仓库
    * 两种场景
        1. 把已有项目代码纳入 Git 管理
        ```
        cd 项目路径
        git init
        ```
        2. 新建的项目直接用 Git 管理
        ```
        cd 某个文件夹
        git init project_name
        cd project_name
        ```
* 工作区、暂存区、版本历史的关系
    * 工作区-->git add . --> 暂存区 --> git commit -m "xxx" -->  版本历史
* git log 查看版本演变历史
    1. git log --all 查看所有分支的历史
    2. git log --all --graph 查看图形化的 log 地址
    3. git log --oneline 查看单行的简洁历史。
    4. git log --oneline -n4 查看最近的四条简洁历史。
    5. git log --oneline --all -n4 --graph 查看所有分支最近 4 条单行的图形化历史。
    6. git help --web log 跳转到git log 的帮助文档网页
* git branch 查看分支
    1. -v 