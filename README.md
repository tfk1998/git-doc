# git常用命令
| 功能              | 指令                            |
| -----------------| ------------------------------  |
| 设置用户名             | `git config --global user.name`+ 你的名字 |
| 查看用户名             | `git config --global user.name` |
| 设置邮箱               | `git config --global user.email`+ 邮箱名 |
| 查看邮箱              | `git config --global user.email` |
| 初始化git仓库          | `git init`                       |
| 查看 global 配置       | `git config --global --list`   |
| 查看当前仓库配置        | `git config --local --list`   |
| 查看变更情况            | `git status`   |
| 添加所有文件到暂存区   | `git add .`(不建议) |
| 添加指定文件到暂存区   | `git add`+文件名(可以多个) |
| 添加所有变化的文件到暂存区   | `git add -A` |
| 将暂存区文件提交到本地仓库   | `git commit -m`+ 描述信息 |
| 比较工作区和暂存区的所有差异   | `git diff` |
| 比较某文件工作区和暂存区的差异   | `git diff`+文件名 |
| 把本地仓库的提交推送到远程仓库   | `git push` |
| 打印所有的提交记录   | `git log` |
| 列出已经存在的远程仓库   | `git remote` |
| 在当前目录下克隆远程仓库到本地  | `git clone`+url              |
| 在当前目录下克隆远程仓库指定分支到本地  | `git clone -b`+分支名 +url|
| 把本地仓库的提交推送到指定远程仓库   | `git push origin`+分支名 |
| 将所有改动文件保存到暂存区   | `git stash` |
| 将所有暂存区文件取出到工作区   | `git stash pop` |
| 切换到指定分支   | `git checkout`+分支名 |
| 将工作区指定文件恢复成和暂存区一致   | `git checkout`+`文件名`(可以多个) |
| 将暂区指定文件恢复成和 HEAD 一致   | `git reset`+文件名(可以多个) |
| 将暂存区和工作区所有文件恢复成和 HEAD 一样   | `git reset --hard` |
| 添加远程仓库   | `git remote add <remote-name> <remote-url>` |

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

#### 规范commit 的好处
- 便于程序员对提交历史进行追溯，便于快速查找信息
- 一旦约束了commit message,每行代码作用、每个功能，颗粒度尽可能细
- 格式化的commit message才可以用于自动化输出Change log
- 统一团队的 Git 工作流，包括分支使用、tag 规范、issue 等
- 提供更多的信息，方便排查与回退

![git](https://user-images.githubusercontent.com/58834537/224219830-578a574f-9c16-43f7-8aab-8f5e5116ebb9.png)
