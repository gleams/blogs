# 安装错误
```
Win10系统 安装 nrm 出现报错：
nrm : 无法加载文件 C:\Program Files\nodejs\yarn.ps1，因为在此系统上禁止运行脚本。有关详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的 about_Execution_Policies。
所在位置 行:1 字符: 1
```
# 解决方法

## 解决办法：

1. win键 + s 搜索 `powershell` 并一`管理员身份`运行：
2. 执行以下命令：set-ExecutionPolicy RemoteSigned 回车；

---