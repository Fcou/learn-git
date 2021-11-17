# Learn Git
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
