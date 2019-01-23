# 2019 深度学习初学者秘技! 轻松备妥NVIDIA GPU深度学习高速运算环境.  
**续集** 这是 2018 深度学习初学者秘技! 轻松备妥NVIDIA GPU深度学习高速运算环境 的续集. http://sina.lt/fSaT 


**重大突破**
1. 支援最新的NVIDIA图灵GPUs -------(开机选项1, 在预设中启动)
2. 把你的NVIDIA GPU桌机变成私人云服务器 --(开机选项2, 已预先安装, 但没有启动)**(选用,非必要)**  

**包括**
1. Ubuntu 18.04
2. NVIDIA CUDA 10
3. Docker CE
4. NVIDIA support for Docker CE
5. Tensorflow/Keras Docker Image for CUDA 10

   (找很久了吧?)  
   (最新的NVIDIA图灵GPUs需搭配CUDA 10, 然而Docker Hub Tensorflow:Tensorflow还没有发布支援CUDA 10的Docker Image)  
   (我这份映像档配备有支持CUDA 10的Tensorflow/Keras Docker Image, 这是目前大家一直找不到的)  
   
6. 按照以下指示, 启动/配置你的NVIDIA GPU桌机变成私人云服务器 **(选用,非必要)**  

   (无敌价值! 打造你专属的深度学习云服务器, 在任何时间, 任意地点远程使用)

___
___
# 开始之前:
**参考2018 深度学习初学者秘技! 轻松备妥NVIDIA GPU深度学习高速运算环境. http://sina.lt/fSaT**
  
___
___
# 开机选项1: 本地使用(Local use), 在预设中启动.  
**下载, 还原, 使用. 就这麽简单:** 
1. NVIDIA 高端 GPU 显示卡.
2. 在这里下载 2019最新的映像档案 (22GB) 百度網盤 链接：https://pan.baidu.com/s/1_euKhqwJY3k0fVDhs_AvUQ 密码：sskt
3. 用Acronis True Image 2018, 把映像档还原到一只高速USB随身碟或是一颗硬碟上.
4. 设定主机板BIOS, 从这只高速USB随身碟或这颗硬碟开机.
5. 重新开机, 开始使用. 就这麽简单!

   Jupyter notebook 在开机後会自动展开.  
   不再需要每次都输入指令: $ sudo docker start -ai tensorflowkeras 與 # jupyter notebook --allow-root.  
   我已为你做了一个无脑自动启动的开机程序.  

___
___
# 开机选项2: 云端使用(Cloud use), 已预先安装, 但没有启动.  
**买神奇工具, 注册/启用 Ngrok 与 Teamviewer, 切换开机选项2:**
1. 买神奇工具, 从手机开/关你的电脑电源.

   推荐傻多"Sapido WSG70n". (任何同等於傻多"Sapido WSG70n"的神奇工具也都能用)
   
2. 设定主机板BIOS. 

   在电源管理选单里, 设定当插座电力恢复供电的时候, 永远自动开启电脑.

3. 注册/启用 Ngrok

   Ngrok已预先下载到目录/home/nvidia/startup, 你唯一要做的事, 是注册/启用ngrok.  
   浏览器连到 https://ngrok.com/, 注册并登入.  
   
   (3-1). 找到你的token令牌, 存进ngrok app里:  
          浏览器连到 https://dashboard.ngrok.com/get-started  
          跳到页面第三步骤connect to your account, 复制 "./ngrok authtoken ....(你的token令牌)"  
          ![](/photo/2019%200a%20Ngrok%20Step%203%20find%20token.png)  
          Ctrl+Alt+T打开终端机, 输入指令:  
          $ cd /home/nvidia/startup  
          $ ./ngrok authtoken ....(你的token令牌)  
          
   (3-2). 订阅 $5美金/每月 ngrok服务:
          ![](/photo/2019%200b%20Ngrok%20Go%20Reserved%20-%20not%20paid%20yet.png)
          ![](/photo/2019%200c%20Ngrok%20Choose%20Subscription.png)
          
   (3-3). 设置 reservered subdomain名称:
          ![](/photo/2019%200d%20Ngrok%20Go%20Reserved%20-%20Setup%20after%20paid.png)
          帮你的subdomain name取一个响亮的名称 xxxxxx, 以後 http://xxxxxx.ngrok.io 就是你的私人云服务器网址. 
          
   (3-4). 把你的subdomain name名称写入startup_opt2_cloud_use.sh开机程序中:  
          Ctrl+Alt+T打开终端机, 输入指令:  
          $ cd /home/nvidia/startup  
          $ sudo nano startup_opt2_cloud_use.sh  
          这会开启一个编辑视窗, 用以上你取的subdomain name名称, 取代下图黄色标记文字.  
          ![](/photo/2019%200e%20Ngrok%20-%20update%20startup_opt2_cloud_use%20sh.png)  
          Ctrl+O存档, Enter键覆盖原档, Ctrl+X退出.  
          
4. Ubuntu startup application设置:  
   关闭 (取消打勾) Startup Opt1, 改启动 (打勾) Startup Opt2  
   ![](/photo/2019%201a%20startup%20applications.png)  
   预设是打勾 Startup Opt1 ==> 本地使用(Local Use)  
   ![](/photo/2019%201b%20startup%20applications%20default.png)  
   预设关闭 (取消打勾) Startup Opt1, 改启动 (打勾) Startup Opt2 ==> 改成云端使用(Cloud Use)  
   ![](/photo/2019%201c%20startup%20applications%20check%20opt2%20uncheck%20opt1.png)  
   
5. TeamViewer开机自启动 设置:  
   开机自启动 Start at boot + 指定权限给你自己 Assign to yourself  
   ![](/photo/2019%202a%20TeamViewer%20Start%20at%20boot%20and%20Assign%20to%20yourself.png)  
   指定权限给你自己 Assign to yourself (用你注册teamviewer帐号的email address)  
   ![](/photo/2019%202b%20TeamViewer%20Assign%20to%20yourself.png)  
   设定固定密码 Change Password + 给予快速通关权限 Grant Easy Access  
   ![](/photo/2019%202c%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)
   设定固定密码 Change Password + 给予快速通关权限 Grant Easy Access  
   ![](/photo/2019%202d%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)  
   重启电脑.

6. 随时随地, 远程使用你的深度学习云服务器   
   拿起你的手机, 透过神奇工具, 远端开启摆在你家里/公司里的桌上型电脑, 自动启动云服务  
   拿起另一台笔记型电脑, 浏览器开启你的私人云服务器网址 http://xxxxxx.ngrok.io  
   随心所欲, 远程使用能NVIDIA GPU高速运算的深度学习Jupyter Notebook程式编辑器   
   ![](/photo/2019%203a%20Access%20your%20DL%20Cloud%20anywhere%20anytime.png) . 

___
___
# 现在展示给也在做深度学习程式的朋友看, 感受他们欣羡的眼光.
**如果你喜欢我的分享, 请你也分享我的Github连结到微信/QQ/微博上.**
https://github.com/Sniper711/2019-DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant/blob/master/README%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87.md

