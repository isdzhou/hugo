---
title: "Win相关"
date: 2024-11-07T11:48:13+08:00
draft: false
tags: ["win"]
categories: ["win"]
description: ""
---

## winget 彩虹进度条

```json
# winget settings

{
    "visual": {
        "progressBar": "rainbow"
    }
}
```

## win11右键菜单修改win10样式

```bash
# cmd
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
# win11
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /va /f
```

## win终端 ssh

```shell
# .ssh 目录新建文件config
# 保持心跳
Host *
    ServerAliveInterval 40

# 别名登录
Host name
    HostName ip
    User root
  	Port 22
    IdentityFile ~/.ssh/OpenCloudOS.pem

Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/GitHub

# 添加ssh密钥代理
ssh-add ~/.ssh/id_rsa
# 查看
ssh-add -l
# 删除
ssh-add -d ~/.ssh/id_rsa   # 删除指定密钥
ssh-add -D                  # 删除全部
```

## 隐藏设置主页

```shell
regedit
计算机\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer
键: SettingsPageVisibility
值: hide:home
```

## 本地账户激活

```shell
# shift + F10
start ms-cxh:localonly
```

## 自动登陆

- regedit 打开注册表
- **AutoAdminLogon**：数值数据设置为 `1` (表示开启自动登录)。
- **DefaultUserName**：数值数据填入你的**账户名**（微软账户则填完整的邮箱地址）。
- **DefaultPassword**：数值数据填入你的**登录密码**。如果这个项目不存在，需要手动新建。
