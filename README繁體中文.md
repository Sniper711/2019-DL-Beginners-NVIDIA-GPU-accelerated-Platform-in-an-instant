# 2019 深度學習初學者祕技! 輕鬆備妥NVIDIA GPU深度學習高速運算環境.  
**續集** 這是 2018 深度學習初學者祕技! 輕鬆備妥NVIDIA GPU深度學習高速運算環境 的續集. https://goo.gl/yMcZMd  


**突破性的進展**
1. 支援最新的NVIDIA圖靈GPUs -------(開機選項1, 在預設中啟動)
2. 把你的NVIDIA GPU桌機變成極貴重的私人雲服務器 --(開機選項2, 已預先安裝, 但沒有啟動)**(選用,非必要)**  

**包括**
1. Ubuntu 18.04
2. NVIDIA CUDA 10
3. Docker CE
4. NVIDIA support for Docker CE
5. Tensorflow/Keras Docker Image for CUDA 10

   (最新的NVIDIA圖靈GPUs需搭配CUDA 10, 然而Docker Hub Tensorflow:Tensorflow還沒有發布支援CUDA 10的Docker Image)
   (我這份映像檔配備有支持CUDA 10的Tensorflow/Keras Docker Image)
   
6. 按照以下指示, 啟動/配置你的NVIDIA GPU桌機變成極貴重的私人雲服務器 **(選用,非必要)**  

   (無敵價值! 打造你專屬的深度學習雲服務器, 在任何時間, 任意地點遠程使用)

___
___
# 開始之前:
**參考2018 深度學習初學者祕技! 輕鬆備妥NVIDIA GPU深度學習高速運算環境. https://goo.gl/yMcZMd**
  
___
___
# 開機選項1: 本地使用(Local use), 在預設中啟動.  
**下載, 還原, 使用. 就這麼簡單:** 
1. NVIDIA 高端 GPU 顯示卡.
2. 在這裡下載 2019最新的映像檔案 (22GB) 
3. Recover with Acronis True Image application, on a high speed USB Disk or HDD/SSD Disk.
4. Set motherboard BIOS to boot from recovered high speed USB Disk or HDD/SSD Disk.
5. Boot PC and ready to use. So Easy!

   Jupyter notebook will automatically pop up.  
   No need to input commands: $ sudo docker start -ai tensorflowkeras & # jupyter notebook --allow-root.  
   I already made a no-brainer autorun shell on Ubuntu startup applications for you.  

___
___
# Starup Option 2: Cloud use, pre-installed, need to be activated.  
**Buy Gadget, Register/Activate Ngrok & Teamviewer, :**
1. Buy gadget to turn on/off PC Power over your phone.

   Recommend "Sapido WSG70n", designed and made in Taiwan. (any "Sapido WSG70n" equivalent gadget works)
   
2. Setup motherboard BIOS. 

   On power management setting, set when Power is ON, then Always Turn On PC.

3. Register/Activate ngrok

   Ngrok is already downloaded into /home/nvidia/startup, what you need is to register/activate ngrok.  
   Visit https://ngrok.com/, register and login.  
   
   (3-1). Find your token and save it to ngrok app:  
          Visit https://dashboard.ngrok.com/get-started  
          Jump to step 3 : connect to your account, copy "./ngrok authtoken ....(your token)  
          ![](/photo/2019%200a%20Ngrok%20Step%203%20find%20token.png)  
          Ctrl+Alt+T open terminal, input the commands:  
          $ cd /home/nvidia/startup  
          $ ./ngrok authtoken ....(your token)  
          
   (3-2). Subscript $5/month ngrok service:
          ![](/photo/2019%200b%20Ngrok%20Go%20Reserved%20-%20not%20paid%20yet.png)
          ![](/photo/2019%200c%20Ngrok%20Choose%20Subscription.png)
          
   (3-3). Setup reservered subdomain name:
          ![](/photo/2019%200d%20Ngrok%20Go%20Reserved%20-%20Setup%20after%20paid.png)
          Choose a favorate subdomain name xxxxxx, now the http://xxxxxx.ngrok.io is your Cloud Service url. 
          
   (3-4). Save setting to startup_opt2_cloud_use.sh
          Ctrl+Alt+T open terminal, input the commands:  
          $ cd /home/nvidia/startup  
          $ sudo nano startup_opt2_cloud_use.sh  
          On pop up window, replace below yellow marked text with your favoraye subdomain name on above.  
          ![](/photo/2019%200e%20Ngrok%20-%20update%20startup_opt2_cloud_use%20sh.png)  
          Ctrl+O to save, Enter to save with current file name, Ctrl+X to exit.  
          
3. Ubuntu startup application settings:  
   De-activate (uncheck) Startup Opt1, Activate (check) Startup Opt2  
   ![](/photo/2019%201a%20startup%20applications.png)  
   By default, Startup Opt1 is checked  
   ![](/photo/2019%201b%20startup%20applications%20default.png)  
   De-activate (uncheck) Startup Opt1, Activate (check) Startup Opt2  
   ![](/photo/2019%201c%20startup%20applications%20check%20opt2%20uncheck%20opt1.png)  
   
4. TeamViewer auto launch settings:  
   Start at boot + Assign to yourself  
   ![](/photo/2019%202a%20TeamViewer%20Start%20at%20boot%20and%20Assign%20to%20yourself.png)  
   Assign to yourself (use your own teamviewer account email address)  
   ![](/photo/2019%202b%20TeamViewer%20Assign%20to%20yourself.png)  
   Change Password + Grant Easy Access  
   ![](/photo/2019%202c%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)
   Change Password + Grant Easy Access  
   ![](/photo/2019%202d%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)  
   Restart your Ubuntu PC.

5. Remotely access your DL Cloud anywhere anytime . 
   Use browser on another laptop, connect to your Cound Service url http://xxxxxx.ngrok.io  
   Start using Jupyter Notebook with NVIDIA GPU accelerated Platform in Cloud remotely  
   ![](/photo/2019%203a%20Access%20your%20DL%20Cloud%20anywhere%20anytime.png) . 

___
___
# Now show it to your Deep Learning coding mates, enjoy their envy.
**If you like my job, please share this Github link out.**
https://github.com/Sniper711/2019-DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant/blob/master/README.md
