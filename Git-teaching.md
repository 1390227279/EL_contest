# Git-teaching
## 获取代码
1. 获取仓库的远程地址（以 GitHub 为例）：

打开 GitHub 仓库页面 → 点击绿色的 Code 按钮。
复制 HTTPS 或 SSH 地址（例如）：
https://github.com/用户名/仓库名.git
git@github.com:用户名/仓库名.git

2. 在终端执行克隆命令：

在文件处打开git bash(和软工克隆一样)
git clone https://github.com/用户名/仓库名.git
如果想克隆到指定目录（如 my-project）：
git clone https://github.com/用户名/仓库名.git my-project

## 查看别人的更改
1. 方法 1：直接拉取最新代码（git pull）
打开终端（Windows：Git Bash / CMD；Mac/Linux：Terminal）。

进入你的本地仓库目录：

bash
cd /path/to/your/repository
拉取远程仓库的最新修改：

bash
git pull origin main  (默认分支通常是 main 或 master)
这会自动下载远程仓库的更新并合并到你的本地分支。

查看更新的内容：

运行 git log 查看最新的提交记录：

bash
git log --oneline  # 简洁显示提交历史
或者用 git diff 对比本地和远程的差异：

bash
git diff HEAD..origin/main  # 比较本地和远程 main 分支的差异
方法 2：仅查看更新，不自动合并（git fetch + git log）
如果你只想先看看别人改了啥，再决定是否合并：

获取远程仓库的最新数据（但不自动合并）：

bash
git fetch origin
查看远程分支的更新：

bash
git log origin/main  # 查看远程 main 分支的提交历史
对比本地和远程的差异：

bash
git diff main origin/main  # 比较本地 main 和远程 main 的区别
手动合并（如果需要）：

bash
git merge origin/main  # 将远程更新合并到本地
方法 3：在 GitHub 网页上直接查看
如果不想用命令行，可以直接在 GitHub 上查看：

打开你的仓库页面，点击 Code 选项卡。

查看 Commits（提交记录），这里会显示所有人推送的修改。

点击某个提交（commit）即可查看具体改动了哪些文件。

关键注意事项
对方必须已 push 到远程仓库，否则你看不到他们的本地修改。

你有权限拉取（Read 权限以上），否则会报错 Permission denied。

如果对方在私人分支工作，你可能需要先切换分支：

bash
git checkout branch_name  # 切换到他们的分支
git pull origin branch_name  # 拉取该分支的更新
