# 2019-DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant  
**Sequel** of 2018 DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant https://goo.gl/LPWr1v  


**Breakthroughs**
1. Support the latest NVIDIA Tuning GPUs -------(Option 1, activated by default)  
2. Deploy your NVIDIA GPU Desktop as an inestimable value Cloud service --(Option 2, pre-installed, not activated yet)**(Optional)**  

**Includes**
1. Ubuntu 18.04
2. NVIDIA CUDA 10
3. Docker CE
4. NVIDIA support for Docker CE
5. Tensorflow/Keras Docker Image for CUDA 10

   (Search it for a long time?)  
   (The latest NVIDIA Turing GPUs requires CUDA 10, however Docker Hub Tensorflow:Tensorflow does not release Docker Image that supports CUDA 10 yet)  
   (This image equips you Tensorflow/Keras Docker Image for CUDA 10)
   
6. Follow instructions hereunder to activate/deploy your GPU Desktop become an inestimable valueCound service **(Optional)**  

   (Supreme value to have your personal Deep Learning cloud server conveniently anytime anywhere)

___
___
# Before you use:
**Refer to 2018 DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant https://goo.gl/LPWr1v**
  
___
___
# Starup Option 1: Local use, by default.  
**Download, Recover, and Use it no-brainer:** 
1. NVIDIA highend GPU Graphic Card.
2. Download 2019 new image file (22GB) 
3. Recover with Acronis True Image application, on a high speed USB Disk or HDD/SSD Disk.
4. Set motherboard BIOS to boot from recovered high speed USB Disk or HDD/SSD Disk.
5. Boot PC and ready to use. So Easy!

   Jupyter notebook will automatically pop up.  
   No need to input commands: $ sudo docker start -ai tensorflowkeras & # jupyter notebook --allow-root.  
   I already made a no-brainer autorun shell on Ubuntu startup applications for you.  

___
___
# Starup Option 2: Cloud use, pre-installed, need to be activated. **(Optional)**    
**Buy Gadget, Register/Activate Ngrok & Teamviewer, Switch to Startup Option 2:**
1. Buy gadget to turn on/off PC Power over your phone.

   Recommend "Sapido WSG70n", designed and made in Taiwan. (any "Sapido WSG70n" equivalent gadget works)
   
2. Setup motherboard BIOS. 

   On power management setting, set when Power is ON, then Always Turn On PC.

3. Register/Activate ngrok

   Ngrok is already downloaded into /home/nvidia/startup, what you need is to register/activate ngrok.  
   Visit https://ngrok.com/, register and login.  
   
   (3-1). Find your token and save it to ngrok app:  
          Visit https://dashboard.ngrok.com/get-started  
          Jump to step 3 : connect to your account, copy "./ngrok authtoken ....(your token)"  
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
          
   (3-4). Save your subdomain name into startup_opt2_cloud_use.sh:
          Ctrl+Alt+T open terminal, input the commands:  
          $ cd /home/nvidia/startup  
          $ sudo nano startup_opt2_cloud_use.sh  
          On pop up window, replace below yellow marked text with your favoraye subdomain name on above.  
          ![](/photo/2019%200e%20Ngrok%20-%20update%20startup_opt2_cloud_use%20sh.png)  
          Ctrl+O to save, Enter to save with current file name, Ctrl+X to exit.  
          
4. Ubuntu startup application settings:  
   De-activate (uncheck) Startup Opt1, Activate (check) Startup Opt2  
   ![](/photo/2019%201a%20startup%20applications.png)  
   By default, Startup Opt1 is checked ==> Local Use  
   ![](/photo/2019%201b%20startup%20applications%20default.png)  
   De-activate (uncheck) Startup Opt1, Activate (check) Startup Opt2 ==> change to Cloud Use  
   ![](/photo/2019%201c%20startup%20applications%20check%20opt2%20uncheck%20opt1.png)  
   
5. TeamViewer auto launch settings:  
   Start at boot + Assign to yourself  
   ![](/photo/2019%202a%20TeamViewer%20Start%20at%20boot%20and%20Assign%20to%20yourself.png)  
   Assign to yourself (use your own teamviewer account email address)  
   ![](/photo/2019%202b%20TeamViewer%20Assign%20to%20yourself.png)  
   Change Password + Grant Easy Access  
   ![](/photo/2019%202c%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)
   Change Password + Grant Easy Access  
   ![](/photo/2019%202d%20TeamViewer%20Change%20Password%20and%20Grant%20Easy%20Access.png)  
   Restart your Ubuntu PC.

6. Remotely access your DL Cloud anywhere anytime  
   Use your phone, turn on Desktop PC power (at home or office) through gadget remotely.
   Use another laptop, connect browser to your Cound Service url http://xxxxxx.ngrok.io  
   Start using Jupyter Notebook with NVIDIA GPU accelerated Platform in Cloud remotely  
   ![](/photo/2019%203a%20Access%20your%20DL%20Cloud%20anywhere%20anytime.png)  

___
___
# Now show it to your Deep Learning coding mates, enjoy their envy.
**If you like my sharing, please share this Github link to your FB.**
https://github.com/Sniper711/2019-DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant/blob/master/README.md
