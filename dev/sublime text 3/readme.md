## settings

```json
{
    "draw_white_space": "all",
    "font_face": "YaHei Consolas Hybrid",
    "ignored_packages": ["Vintage"]
}
```

## keymap

```json
[
    {
        "keys": ["ctrl+s"],
        "command": "save_all"
    },
    {
        "keys": ["ctrl+w"],
        "command": "close_all"
    },
    {
        "keys": ["escape"],
        "command": "close"
    }
]
```

## Package Control

通过快捷键 ctrl+` 或者 View > Show Console 菜单打开控制台，粘贴代码后回车安装

```python
import  urllib.request,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();urllib.request.install_opener(urllib.request.build_opener(urllib.request.ProxyHandler()));open(os.path.join(ipp,pf),'wb').write(urllib.request.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())
```

## Packages

按 Ctrl+Shift+P 后输入 install package ：

-   SideBarEnhancements
-   ConvertToUTF8
-   CodeFormatter
