設定Unity開發環境
========================================

Android版環境設定
----------------------------------------

本文件說明如何設定Unity輸出Android版本遊戲的開發環境，以下列出目前使用的平台:
   
   * Windows 7 64 bit
   * Unity 5.3.0f4 Personal


1.下載並安裝
   .. image:: /_static/image/setup-build-environment/1_install_jdk.png


2.下載 `Android SDK <https://developer.android.com/sdk/installing/index.html>`_，可安裝Stand-alone SDK Tools即可
   安裝完成後，到安裝目錄開啟SDK Manager.exe
   
   * 預設安裝目錄是 ``C:\Users\[YOUR_USER_NAME]\AppData\Local\Android\android-sdk``
   * 或是全域的的目錄 ``C:\Program Files (x86)\Android\android-sdk``

   將下列的工具和SDK打勾並安裝
   
   .. image:: /_static/image/setup-build-environment/2_androidsdkmanager_0.png
   .. image:: /_static/image/setup-build-environment/2_androidsdkmanager_1.png


3.安裝完成後到Unity的”Menu > Edit > Preferences“
   將Android SDK Location和JDK Location設定好
   
   預設值分別是
   
   * ``C:\Users\[YOUR_USER_NAME]\AppData\Local\Android\android-sdk`` (Android SDK預設目錄)
   * ``C:\Program Files (x86)\Android\android-sdk`` (Android SDK全域目錄)
   * ``C:\Program Files\Java\jdk1.8.0_05`` (JDK版本可能不同)
   
   .. image:: /_static/image/setup-build-environment/3_unity_preferences.png
   
   
4.設定Build Settings
   Unity的”File > Build Settimgs”開啟建置設定
   確定目前是平台Android，選擇Player Settings進入Android設定

   .. image:: /_static/image/setup-build-environment/4_unity_buildsettings.png
   
   
5.設定PlayerSettings

   .. warning:: 因為還沒有正式發佈，所以這些值可以先用暫代值

   * Company Name代表公司或開發單位名稱
   * Product Name表示產品名稱，Android選單顯示在icon下的文字
   * 注意Bundle Identifier是否有正確，這個值是Google Play上遊戲的唯一ID，上架的時候必須和商店的ID一致
   * Bundle Version是版本，可以是字串，用來讓一般使用者辨識的版號
   * Bundle Version Code是內部用版號，純數字且每經過一次發佈這個版號必須比上次的值還要高

   .. image:: /_static/image/setup-build-environment/5_unity_playersettings.png


6.上述設定完成後就可以用Build或是Build And Run來建置apk檔
   Build And Run會在build完後自動將apk傳至手機並啟動，所以要先把手機接到USB並開啟開發者模式

   .. image:: /_static/image/setup-build-environment/6_unity_buildsettings.png

7. .. note:: 正式發佈設定(未完)


iOS版環境設定
----------------------------------------

