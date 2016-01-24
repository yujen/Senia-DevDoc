Unity輸入圖檔的設定
========================================


Unity輸入圖檔的設定請修改以下設定
   .. image:: /_static/image/howto-import-texture/0_step.png

  * Texture Type : 使用Sprite(2D and UI)
  * Sprite Mode : Single
  * Packing Tag : 有相同tag的圖檔在build apk時會被包成相同一張圖以增加效能，使用連續動畫時加入tag，把一連串的動作做成同一個atlas
  * Pixels Per Unit : 選1表示一個pixel當單位
  * Pivot : 選Center當中心
  * Generate Mip Maps : 不要勾選這個選項，這個是給3D模型做LOD用的
  * Filter Mode : 選Trilinear減少在縮放時產生鋸齒
  * Max Size : 行動裝置小於2048比較好
  * Format : 選Turecolor，讓SeniaSpritePackPolicy去做最後的壓縮設定

Sprite Packer工具
   .. image:: /_static/image/howto-import-texture/1_step.png
   
  * 選擇“Menu -> Window -> Sprite Packer”，開啟Sprite Packer可以用來檢查有哪些圖檔會被加入atlas
  * 若一開始畫面是空的，先確認圖檔有先設定Packing Tag，然後點選Pack產生atlas
  * View atlas : Unity會根據Packing Tag產生下拉式選單，選擇相對應的名稱來切換檢視atlas
  * 將DefaultPackerPolicy改成SeniaSpritePackPolicy這個客製化的atlas輸出法
  * 中央的圖會顯示多張圖檔包成atlas的結果，注意不要讓解析度超過2048x2048

