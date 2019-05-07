### 我们经常需要用自己的笔记本连接实验室或者公司的GPU服务器来运行代码。百度上也没有找到详细的步骤，所以自己整理了一份。

- **需要的软件**
  - Xmanager (Xshell) 或 putty 用于连接服务器
  - WinSCP 用于远端传输数据和文件等，例如把笔记本的代码传到服务器中。
  
    （该软件只需要window用户下载，Linux系统自带scp命令）
  - 天域INET 用于跨网段连接（用网线的话不需要下载）
   
- **需要知道的，重要！！**
  - 服务器的IP，用户名，密码
  
- **如何操作**
  - 连接天域INET（用网线不用）
  - 打开Xshell，文件-->新建-->输入用户名和IP
  - 打开WinSCP,输入ip,用户名和密码登录，然后可以拖拽式传输文件
  - 在Xshell中运行程序即可
  
- **如何使用服务器并且在自己的浏览器中打开jupyter notebook**

  在Xshell中输入 jupyter notebook --ip 服务器IP地址,然后复制下面出现的网址到自己的浏览器即可打开。    
  指定端口：jupyter notebook --no-browser --port 6000 --ip=192.168.1.103
  
- 使用服务器中需要注意的点
  - 指定GPU操作
  
  > import os
  
  > os.environ\["CUDA_VISIBLE_DEVICES"]="0"
  - 查看GPU使用情况
  > nvidia-smi
