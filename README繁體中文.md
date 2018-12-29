# 2019 深度學習初學者祕技! 輕鬆備妥NVIDIA GPU深度學習高速運算環境.  
**續集** 這是 2018 深度學習初學者祕技! 輕鬆備妥NVIDIA GPU深度學習高速運算環境 的續集. https://goo.gl/yMcZMd  


**重大突破**
1. 支援最新的NVIDIA圖靈GPUs -------(開機選項1, 在預設中啟動)
2. 把你的NVIDIA GPU桌機變成極貴重的私人雲服務器 --(開機選項2, 已預先安裝, 但沒有啟動)**(選用,非必要)**  

**包括**
1. Ubuntu 18.04
2. NVIDIA CUDA 10
3. Docker CE
4. NVIDIA support for Docker CE
5. Tensorflow/Keras Docker Image for CUDA 10

   (找很久了吧?)
   (最新的NVIDIA圖靈GPUs需搭配CUDA 10, 然而Docker Hub Tensorflow:Tensorflow還沒有發布支援CUDA 10的Docker Image)
   (我這份映像檔配備有支持CUDA 10的Tensorflow/Keras Docker Image, 這是目前大家一直找不到的)
   
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
3. 用Acronis True Image 2018, 把映像檔還原到一只高速USB隨身碟或是一顆硬碟上.
4. 設定主機板BIOS, 從這只高速USB隨身碟或這顆硬碟開機.
5. 重新開機, 開始使用. 就這麼簡單!

   Jupyter notebook 在開機後會自動展開.  
   不再需要每次都輸入指令: $ sudo docker start -ai tensorflowkeras 與 # jupyter notebook --allow-root.  
   我已為你做了一個無腦自動啟動的開機程序.  

___
___
# 開機選項2: 雲端使用(Cloud use), 已預先安裝, 但沒有啟動.  
**買怪給西, 註冊/啟用 Ngrok 與 Teamviewer, 切換開機選項2:**
1. 買怪給西, 從手機開/關你的電腦電源.

   推薦傻多"Sapido WSG70n", 完全由台灣設計與製造的產品. (任何同等於傻多"Sapido WSG70n"的怪給西也都能用)
   
2. 設定主機板BIOS. 

   在電源管理選單裡, 設定當插座電力恢復供電的時候, 永遠自動開啟電腦.

3. 註冊/啟用 Ngrok

   Ngrok已預先下載到目錄/home/nvidia/startup, 你唯一要做的事, 是註冊/啟用ngrok.  
   瀏覽器連到 https://ngrok.com/, 註冊並登入.  
   
   (3-1). 找到你的token令牌, 存進ngrok app裡:  
          瀏覽器連到 https://dashboard.ngrok.com/get-started  
          跳到頁面第三步驟connect to your account, 複製 "./ngrok authtoken ....(你的token令牌)"  
          ![](/photo/2019%200a%20Ngrok%20Step%203%20find%20token.png)  
          Ctrl+Alt+T打開終端機, 輸入指令:  
          $ cd /home/nvidia/startup  
          $ ./ngrok authtoken ....(你的token令牌)  
          
   (3-2). 訂閱 $5美金/每月 ngrok服務:
          ![](/photo/2019%200b%20Ngrok%20Go%20Reserved%20-%20not%20paid%20yet.png)
          ![](/photo/2019%200c%20Ngrok%20Choose%20Subscription.png)
          
   (3-3). 設置 reservered subdomain名稱:
          ![](/photo/2019%200d%20Ngrok%20Go%20Reserved%20-%20Setup%20after%20paid.png)
          幫你的subdomain name取一個響亮的名稱 xxxxxx, 以後 http://xxxxxx.ngrok.io 就是你的私人雲服務器網址. 
          
   (3-4). 把你的subdomain name名稱寫入startup_opt2_cloud_use.sh開機程序中:  
          Ctrl+Alt+T打開終端機, 輸入指令:  
          $ cd /home/nvidia/startup  
          $ sudo nano startup_opt2_cloud_use.sh  
          這會開啟一個編輯視窗, 用以上你取的subdomain name名稱, 取代下圖黃色標記文字.  
          ![](/photo/2019%200e%20Ngrok%20-%20update%20startup_opt2_cloud_use%20sh.png)  
          Ctrl+O存檔, Enter鍵覆蓋原檔, Ctrl+X退出.  
          
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
