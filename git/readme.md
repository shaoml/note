## 最小配置

```bash
git config --global user.name 'shaoml'
git config --global user.email 'shaoml.cn@gmail.com'

# 缺省等同于 local
# --local 只对某个仓库有效
# --global 对当前用户所有仓库有效
# --system 对系统所有登录的用户有效

# 显示 config 的配置，加 --list
git config --list
git config --list --local
git config --list --global
git config --list --system
```

## SSH 配置

```bash
# 检查现有的 SSH 密钥
ls -al ~/.ssh
# 生成新的 SSH 密钥
ssh-keygen -t ed25519 -C "shaoml.cn@gmail.com"
# 当提示您“输入要在其中保存密钥的文件”时，请按 Enter，接受默认文件位置
# 在提示符下，键入一个安全密码
******************
# 将 SSH 密钥添加到 ssh-agent
# 启动 ssh-agent ，执行
eval $(ssh-agent -s)
# 将 SSH 私钥添加到 ssh-agent ，执行
ssh-add ~/.ssh/id\*ed25519
# 向 GitHub 帐户添加新的 SSH 密钥
# 将 SSH 公钥复制到剪贴板，执行
clip < ~/.ssh/id_ed25519.pub
# 打开 github 设置页面，点击 SSH and GPG keys，点击 New SSH key
# Title：SHAOMLPC，Key：粘贴
\_optional\*
# 设置 ssh-agent 在 Windows 上的 Git 上自动启动
# 复制文件 bash.bashrc 到路径下 C:\Program Files\Git\etc
```
