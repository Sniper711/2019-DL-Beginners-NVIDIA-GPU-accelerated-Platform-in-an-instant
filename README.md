# 2019-DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant
(*page working in process) 
Sequel of 2018 DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant https://goo.gl/LPWr1v 

**Breakthroughs**
1. Support the latest NVIDIA Tuning GPUs -------------(Option 1, activated by default)
2. Deploy your GPU Desktop become a Cloud service --(Option 2, pre-installed, not activated yet)

**Includes**
1. Ubuntu 18.04
2. NVIDIA CUDA 10
3. Docker CE
4. NVIDIA support for Docker CE
5. Tensorflow/Keras Docker Image for CUDA 10

   (The latest NVIDIA Turing GPU requires CUDA 10, however Docker Hub Tensorflow:Tensorflow does not release Docker Image that supports CUDA 10 yet)  
   (This image equips you Tensorflow/Keras Docker Image for CUDA 10)
   
6. Follow instructions hereunder to activate/deploy your GPU Desktop become a Cound service 

   (Supreme value to have your personal Deep Learning cloud server conveniently anytime anywhere)

___
___
# Before you use:
**Refer to 2018 DL-Beginners-NVIDIA-GPU-accelerated-Platform-in-an-instant https://goo.gl/LPWr1v**
  
___
___
# Starup Option 1: Local use, by default.  
**Download, Recover, and Use it no-brainer:** 
1. NVIDIA highend GPU.
2. Download 2019 new image file 
3. Recover with Acronis True Image application, on a high speed USB Disk or HDD/SSD Disk.
4. Set motherboard BIOS to boot from recovered high speed USB Disk or HDD/SSD Disk.
5. Boot PC and ready to use. So Easy!

   Jupyter notebook will automatically pop up.  
   No need to input commands: $ sudo docker start -ai tensorflowkeras & # jupyter notebook --allow-root.  
   I already made a no-brainer autorun shell on Ubuntu startup applications for you.  


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
   
2. Download 2019 new image file here 
3. Recover with Acronis True Image application, make sure you recover to high speed USB Disk or HDD/SSD Disk.
4. Set motherboard BIOS to boot from recovered high speed USB Disk or HDD/SSD Disk.
5. Boot and ready to use. Jupyter notebook will automatically pop up. 
PS. No need to input $ sudo docker start -ai tensorflowkeras & # jupyter notebook --allow-root, because I make a no-brainer shell on Ubuntu startup applications for you. 

Buy 1pcs high speed USB Drive 64GB or 128GB.  
   (Recommend SanDisk Extreme Pro CZ880 128GB, Read/Write=420MBps/380MBps)  
   (Recommend ~~SanDisk Extreme Go CZ800 64GB, Read/Write=200MBps/150MBps~~)  
   USB Drive speed matters, data is frequently accessed during training, please buy 
