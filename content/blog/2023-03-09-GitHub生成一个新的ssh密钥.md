---
slug: 187
title: GitHub 生成一个新的 ssh 密钥
date: 2023-03-09
categories: 
  - 技术
tags: 
  - Github
---

要在 GitHub 上生成新的 SSH 密钥，请按照以下步骤操作：

1. 打开终端或命令提示符。
2. 输入以下命令：将"your_email@example.com"替换为您在 GitHub 上注册的电子邮件地址。
```shell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
3. 稍后您将被提示输入文件保存位置和密码短语。您可以保持所有默认设置，只需一直按 Enter 键即可。
4. 然后输入以下命令：eval "$(ssh-agent -s)"
5. 然后输入以下命令以将新密钥添加到 ssh-agent 中：ssh-add ~/.ssh/id_rsa
6. 最后，请在 GitHub 上添加您的公共密钥。转到 GitHub 设置并单击"SSH and GPG keys "("SSH 和 GPG 密钥"）。
7. 单击“新密钥”按钮。
8. 在“标题”字段中输入一个描述性标题，以便您可以识别此密钥。
9.  在“密钥”字段中，将“~/.ssh/id_rsa.pub”文件中的内容复制并粘贴到文本框中。
10. 单击“添加 SSH 密钥”按钮以保存您的新密钥。

现在，您已经成功为 GitHub 生成了一个新的 SSH 密钥！

来自 chatGPT 的教程，记录一下。
