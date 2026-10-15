# 996 Guardian 游戏守护助手

## 获取完整源码

本次首发完整源码保存在仓库根目录的 `996-guardian-assistant-source.zip`，下载并解压后进入同名目录，再按下方步骤运行或编译。压缩包包含源代码和 MIT 许可证，不包含运行数据或安装包。


Windows C# / .NET Framework 源码，基于 V4.20.10，MIT 开源。

## 功能
雷电模拟器实例绑定、截图识别、地图优先级与寻路、BOSS倒计时调度、自动战斗状态恢复、福利邮件与背包维护、限时重试、诊断日志容量控制。

## 编译
需要64位Windows、.NET Framework 4.x编译器及系统Windows Runtime元数据。
```powershell
powershell -ExecutionPolicy Bypass -File .\编译.ps1
```
编译生成996守护助手.exe。运行前自行安装雷电模拟器、在自己有权使用的环境中准备识别模板并校准。

## 模板与配置
本仓库发布原创代码及路线/BOSS配置，不分发游戏客户端、美术资源、用户截图、账户配置或历史诊断。templates/required-files.txt列出原版本模板文件名；缺少模板时相关视觉功能不可用，源码包不是开箱即用安装包。
- boss-targets.json：BOSS调度配置。
- map-routes.json：地图路线配置。
- route-coordinates.example.json：坐标配置示例。
- 可用data-directory.txt指定本机数据目录；未配置时使用程序目录下data。

## 开发与限制
状态机采用限时等待与失败退让。地图、分辨率或界面发生变化时需重新校准。仅在允许自动化的环境中使用；不包含游戏服务端、账号或第三方二进制依赖。不要提交运行日志、截图、缓存或模拟器文件。

MIT许可仅覆盖原创代码，第三方名称及素材不属于本许可证授权范围。
