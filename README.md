# 学习编程 (Learn Programming)

## 配置全局用户名和邮箱 (Configure Global User Name and Email)

### 步骤1：打开终端配置用户名和邮箱（Step 1: Open the terminal to configure the user name and email）

1. 打开终端 (Open the terminal)
2. 输入以下命令，并回车 (Type the following command and press Enter)

```bash
git config --global user.name "Your Name"
```
```bash
git config --global user.email "your-email@example.com"
```

### 步骤2：验证配置是否成功 (Step 2: Verify the configuration)

1. 打开终端 (Open the terminal)
2. 输入以下命令，并回车 (Type the following command and press Enter)

```bash
git config --global --list
```

## 克隆GitHub仓库到本地 (Clone GitHub Repository to Local)

### 步骤 1: 转至存放仓库的本地目录 (Step 1: Navigate to the directory where you want to clone the repository)

打开终端，导航到你想要存放本地副本的目录。(Open the terminal and navigate to the directory where you want to clone the repository)

```bash
cd ~/Documents/GitHub/  # 例如，假设你习惯将仓库放在 Documents/GitHub 文件夹下 (For example, if you prefer to store the repository in the Documents/GitHub folder)
```

### 步骤 2: 克隆仓库 (Step 2: Clone the repository)

使用 git clone 命令将远程仓库克隆到本地。替换 <https://github.com/username/repository.git> 为实际的仓库URL。(Use the git clone command to clone the repository to your local machine. Replace <https://github.com/username/repository.git> with the actual repository URL.)

```bash
git clone https://github.com/your-username/your-repository.git
```

### 步骤 3: 进入仓库目录 (Step 3: Enter the repository directory)

克隆完成后，进入新创建的仓库目录。(After cloning, enter the repository directory.)

```bash
cd your-repository
```

### 步骤 4: 编辑文件 (Step 4: Edit the files)

使用你喜欢的文本编辑器（如 vim、nano 或直接在VSCode中打开）修改或添加文件。(Use your favorite text editor (such as vim, nano, or directly open it in VSCode) to modify or add files.)

```bash
vim README.md
```

### 步骤 5: 提交更改 (Step 5: Commit the changes)

在做出更改后，使用以下命令将更改添加到暂存区，并提交。(After making changes, use the following commands to add the changes to the staging area and commit them.)

```bash
git add .  # 添加所有改动的文件到暂存区 (Add all modified files to the staging area)
git status  # 可选：查看当前状态，确认待提交的更改 (Optional: View the current status to confirm the changes to be committed)
git commit -m "详细描述你的更改"  # 用有意义的信息提交更改 (Commit the changes with a meaningful message)
```

### 步骤 6: 推送更改到远程仓库Github (Step 6: Push the changes to the remote GitHub repository)

将你的更改推送到远程仓库的主分支（或指定分支）。(Push the changes to the main branch (or a specified branch) of the remote GitHub repository.)

```bash
git push origin main  # 如果主分支名为main；如果是master，则使用git push origin master (If the main branch is named main; if it is master, use git push origin master)
```
## 本地更新
要保持本地仓库与GitHub上的仓库同步，当GitHub仓库有更新时，你需要执行以下步骤：

打开命令行：首先，打开你的终端（如CMD、PowerShell、Terminal或VSCode的终端）。

### 步骤1：导航到本地仓库：使用cd命令切换到本地仓库的根目录。例如：

```bash
cd path/to/your/local/repository # 检查远程状态（可选）：使用git status或git remote update查看远程分支的最新状态，确认是否有更新。
```

### 步骤2：拉取远程更改： 使用git fetch命令获取远程仓库的所有最新更改，但不自动合并到你的工作分支。

```Bash
git fetch origin
```

如果你只想获取特定分支的更新，可以指定分支名，如：

```Bash
git fetch origin main # 其中main是分支名，根据实际情况替换。
```
### 步骤4：查看并合并更改：

查看差异：使用git diff命令查看本地与远程分支之间的差异。
合并更改：使用git merge命令将远程分支的更改合并到你的当前分支。如果之前是git fetch origin main，则执行：
```Bash
git merge origin/main # 如果有冲突，需要手动解决冲突，然后添加并提交解决冲突后的文件。
```
### 替代方案：直接拉取并合并： 如果你确定不会有冲突或者愿意处理可能出现的冲突，可以直接使用git pull命令，它等同于执行git fetch随后git merge。

```Bash
git pull origin main # 这将直接从远程分支main拉取并合并到你的当前分支。
```

完成以上步骤后，你的本地仓库就与GitHub上的仓库保持同步了。记得定期重复这些步骤，特别是当你知道远程仓库有新提交时。
