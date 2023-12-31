

## commit详解



`git commit` 命令用于将已暂存（staged）的更改提交到Git仓库中，创建一个新的提交记录（commit）。每个提交记录都包含了一组更改的描述以及一个唯一的哈希值，用于跟踪项目的历史和版本控制。以下是 `git commit` 命令的详细解释和一些常见用法：

**语法**：
```bash
git commit [-m "提交消息"]
```

**常用选项**：

- `-m "提交消息"`：用于在命令行中直接提供提交消息，以描述本次提交的目的和更改内容。这个消息应该是简明扼要的，以便其他开发者能够理解提交的目的。

**示例用法**：

1. 基本的提交：
   ```bash
   git commit -m "添加新功能"
   ```
   这将提交当前分支上已经暂存的更改，并使用指定的提交消息来创建一个新的提交记录。

2. 多行提交消息：
   ```bash
   git commit -m "添加新功能
   
   这个新功能解决了问题 #123."
   ```
   提交消息可以包含多行文本，但需要在消息开头的引号内包含换行符。

3. 不使用 `-m` 选项：
   ```bash
   git commit
   ```
   如果不使用 `-m` 选项，Git将会打开默认的文本编辑器，以便你可以输入多行提交消息。编辑器通常是配置中设置的默认编辑器，如`vi`、`nano`或`vim`。输入完消息后，保存并关闭编辑器即可完成提交。

4. 修改最后一次提交：
   ```bash
   git commit --amend
   ```
   这个命令允许你修改最后一次提交记录的消息或者添加新的更改到最后一次提交中。它会打开文本编辑器，让你编辑提交消息。

5. 交互式提交：
   ```bash
   git commit -i
   ```
   这个命令会进入交互式提交模式，允许你选择哪些文件要暂存和提交，以及如何提交它们。这对于拆分大型提交或重新排列更改非常有用。

6. 提交全部更改：
   ```bash
   git commit -a -m "提交所有更改"
   ```
   使用 `-a` 选项可以提交所有已修改的文件，而不需要使用 `git add` 将它们暂存。

7. 提交指定文件：
   ```bash
   git commit file1.txt file2.txt -m "提交文件"
   ```
   你可以指定要提交的文件，而不是提交所有更改。
