# Git常用命令
| 功能              | 指令                            |
| -----------------| ------------------------------  |
| 设置用户名             | `git config --global user.name`+ name |
| 查看用户名             | `git config --global user.name` |
| 设置邮箱               | `git config --global user.email`+ email |
| 查看邮箱              | `git config --global user.email` |
| 初始化git仓库          | `git init`                       |
| 查看 global 配置       | `git config --global --list`   |
| 查看当前仓库配置        | `git config --local --list`   |
| 查看变更情况            | `git status`   |
| 列出本地的所有分支       | `git branch`      |
| 列出所有远程分支       | `git branch -r`      |
| 删除远程分支       | `git push origin --delete` +branch-name      |
| 添加所有文件到暂存区   | `git add .`(不建议) |
| 添加指定文件到暂存区   | `git add`+filename(可以多个) |
| 添加所有变化的文件到暂存区   | `git add -A` |
| 将暂存区文件提交到本地仓库   | `git commit -m`+ description |
| 比较工作区和暂存区的所有差异   | `git diff` |
| 比较某文件工作区和暂存区的差异   | `git diff`+filename |
| 把本地仓库的提交推送到远程仓库   | `git push` |
| 打印所有的提交记录   | `git log` |
| 列出已经存在的远程仓库   | `git remote` |
| 在当前目录下克隆远程仓库到本地  | `git clone`+url              |
| 在当前目录下克隆远程仓库指定分支到本地  | `git clone -b`+branch-name +url|
| 把本地仓库的提交推送到指定远程仓库   | `git push origin`+branch-name |
| 将所有改动文件保存到暂存区   | `git stash` |
| 将所有暂存区文件取出到工作区   | `git stash pop` |
| 切换到指定分支   | `git checkout`+branch-name |
| 新建一个分支，并切换到该分支   | `git checkout -b `+branch-name |
| 将工作区指定文件恢复成和暂存区一致   | `git checkout`+filename(可以多个) |
| 将暂区指定文件恢复成和 HEAD 一致   | `git reset`+filename(可以多个) |
| 将暂存区和工作区所有文件恢复成和 HEAD 一样   | `git reset --hard` |
| 添加远程仓库   | `git remote add` +remote-name+remote-url |
| 从远程仓库获取最新版本并合并到本地   | `git pull` |

# commit规范

| 类型         | 详细介绍 |
| ----------- | ----------- |
| feat      | 新功能、新特性   |
| fix	bugfix   | 修改问题        |
|refactor	|代码重构|
|docs	|文档修改|
|style	|代码格式修改，注意不是css修改|
|test	|测试用例修改|
|chore	|其他修改，比如构建，依赖管理|
|merge	|代码合并|
|revert	|回滚到上一个版本|
|perf	|优化相关，比如提升性能、体验|

### 规范commit 的好处
- 便于程序员对提交历史进行追溯，便于快速查找信息
- 一旦约束了commit message,每行代码作用、每个功能，颗粒度尽可能细
- 格式化的commit message才可以用于自动化输出Change log
- 统一团队的 Git 工作流，包括分支使用、tag 规范、issue 等
- 提供更多的信息，方便排查与回退

# Git分支与版本发布规范
#### 基本原则
`master为保护分支，不直接在master上进行代码修改和提交。`
#### 分支命名规范
开发从master分支上checkout一个feature分支进行开发或者fix分支进行bug修复，功能测试完毕并且项目发布上线后，将feature分支合并到主干master，并且打tag发布，最后删除开发分支。
- 分支版本命名规则：分支类型 _ 分支发布时间 _ 分支功能。例如:feat_20201122_login
- 分支类型包括：feat、 fix、refactor三种类型，即新功能开发、bug修复和代码重构
-  时间使用年月日进行命名，不足2位补0
- 分支功能命名使用snake case命名法，即下划线命名

# Git工作流
- Git flow
- Github flow
- Gitlab flow
[参考文献](https://www.ruanyifeng.com/blog/2015/12/git-workflow.html)


# 操作流程
![git](https://user-images.githubusercontent.com/58834537/224219830-578a574f-9c16-43f7-8aab-8f5e5116ebb9.png)
