## KMS 激活

```bash
# 管理员权限打开命令行，依次输入
slmgr.vbs /upk
slmgr /ipk VK7JG-NPHTM-C97JM-9MPGT-3V66T
slmgr /skms kms.xspace.in
slmgr /ato
slmgr /skms 127.0.0.1
```

## 关闭自动更新

```bash
# services.msc -> windows update -> 属性 -> 禁用
sc delete wuauserv
```

## 卸载 IE

控制面板 -> 程序 -> 启用或关闭 windows 功能 -> IE -> 勾除

## 卸载 EDGE

```bash
# 打开 powershell ，输入
get-appxpackage *edge*
# 找到 package full name 下的地址并复制
icacls "C:\Windows\SystemApps\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\*" /grant Users:(F) /T
icacls "C:\Windows\SystemApps\Microsoft.MicrosoftEdgeDevToolsClient_8wekyb3d8bbwe\*" /grant Users:(F) /T
```

文件夹 -> 属性 -> 安全 -> 高级 -> 所有者 -> 当前用户群组
文件夹 -> 属性 -> 安全 -> 编辑 -> 当前用户群组 -> 完全控制
以管理员身份打开 cmd 执行命令
删除文件夹

## 卸载 win10 照片应用

```bash
# 管理员身份打开 powershell， 执行：
get-appxpackage *photo*
# 复制 package full name 下的名称，并执行：
remove-appxpackage Microsoft.Windows.Photos_2018.18051.21218.0_x64__8wekyb3d8bbwe
```

## 替换 win7 照片查看器

1、打开 regedit ，定位到：`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Photo Viewer\Capabilities\FileAssociations`

2、新建字符串值 .jpg .png .gif，数值数据：`PhotoViewer.FileAssoc.Tiff`

## 删除快捷方式文件夹

1、打开 regedit，定位到：
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace`

2、找到对应的注册表项，删除即可：

- 图片： {24ad3ad4-a569-4530-98e1-ab02f9417aa8}
- 音乐： {3dfdf296-dbec-4fb4-81d1-6a3438bcf4de}
- 文档： {d3162b92-9365-467a-956b-92703aca08af}
- 视频： {f86fa3ab-70d2-4fc7-9c99-fcbf05467f3a}
- 桌面： {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}
- 3D 对象： {0DB7E03F-FC29-4DC6-9020-FF41B59E513A}

## PowerShell 权限提升

1、以管理员权限身份打开 PowerShell ，执行 `Set-ExecutionPolicy RemoteSigned`

2、选择 Y ，确认

## 命令行打开当前文件夹

explorer .
