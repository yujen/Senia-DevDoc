Dialog Syntax
========================================

.. error:: 新的文件搬到這邊更新 https://hackmd.io/s/HkI1HAisl


dialog.csv的填法

   category 表示同一連串對話，對話結束時會自動將整個對話UI刪除
   type 表示這一列的功能
   value0~value4 表示參數，由於每個功能需要的參數不同，填0表示沒有用到

LibreOffice開啟csv的設定


.. contents:: type參數目錄
  :local:
  :depth: 1


顯示對話文字 ``SHOW_TEXT``
----------------------------------------

   * value0 角色名
   * value1 對話內容，可使用UGUI支援的BBcode
   * value2 對話時是否要播放角色動畫，值為sprite名稱，例如如sprite_senia
   * value3 開始對話時的動畫(嘴巴)
   * value4 對話結束時的動畫(嘴巴)
   * value5 開始對話時的動畫(眼睛)

   value1 支援UGUI的字體效果標籤
   可以參考文件
   http://docs.unity3d.com/Manual/StyledText.html


設定場景角色圖 ``LOAD_TACHIE``
----------------------------------------

   * value0~value4都可以使用，所以場景中最多可以顯示5個角色
    
     值的內容是sprite的名稱，例如sprite_senia, sprite_elf


移除場景角色圖 ``UNLOAD_TACHIE``
----------------------------------------

   * value0 角色sprite名稱，例如sprite_senia


設定角色位置 ``SET_POS``
----------------------------------------

   * value0~value4都可以使用，表示要設定0~4的位置
    
     值的內容是x,y，例如0,0會把圖移到原點


動畫移動角色圖 ``MOVE_POS``
----------------------------------------

   * value0 立繪名，例如sprite_fairy
   * value1 值的內容是x,y，例如100,0會把圖動畫位移到100,0位置
   * value2 移動時間


將角色圖淡出 ``FADE_OUT``
----------------------------------------

   * value0~value4都可以使用，表示要設定0~4的位置

     值的內容是淡出時間，例如0.5秒


將角色圖淡入 ``FADE_IN``
----------------------------------------

   * value0~value4都可以使用，表示要設定0~4的位置

     值的內容是淡入時間，例如0.5秒


載入背景圖 ``LOAD_BG``
----------------------------------------

   * value0 背景圖名稱，例如background_02
   * value2 淡入時間，例如0.5秒

淡出背景圖 ``FADEOUT_BG``
----------------------------------------

   * value0 淡入時間，例如0.5秒


設定角色動畫 ``SET_ANIM``
----------------------------------------

   value0~value4都可以使用，表示要設定0~4位置的動畫
   值的內容是動畫state名稱，例如anim_senia_mouth_normal
   也可以用逗號一次設定多個動畫，例如anim_senia_eye_normal,anim_senia_mouth_normal

   * value0 角色sprite名稱，如sprite_senia
   * value1 第一個動畫
   * value2 第二個動畫

   名稱可參考下表
   https://docs.google.com/spreadsheets/d/1veEFC_ygWiwXaWbpNiHscTdDrVfX3Tv4qLV8XjoWcww/edit#gid=1848990909




移動對畫框 ``MOVE_DIALOG_UI``
----------------------------------------

   * value0 對畫框預設在-400,0的位置，0,0表示要移到原點



設定腳色sprite的前後順序，表示要設定0~4位置前後順序 ``SET_ORDER``
--------------------------------------------------------------------------------

   * value0~value4代表0~4位置的sprite順序，建議使用值10、20、30，避免跟其他sprite衝突



設定角色圖參數 ``SET_SPRITE``
----------------------------------------

   * value0 角色sprite名稱，例如sprite_senia
   * value1 角色位置，例如0,-200
   * value2 角色圖顏色，例如0.5,0.5,0.5,1.0
   * value3 角色圖順序，建議使用值10、20、30，避免跟其他sprite衝突



設定背景音樂 ``SET_BGM``
----------------------------------------

   * value0 音樂檔名，例如battle01
   * value1 淡入淡出時間，例如2.5



回復對話前的BGM ``REVERT_BGM``
----------------------------------------

   * value0 淡入淡出時間，例如1秒



震動畫面 ``SHAKE_CAMERA``
----------------------------------------

   * value0 震動大小
   * value1 震動時間


載入sprite ``LOAD_SPRITE``
----------------------------------------

   * value0 放在Resources/AssetBundles/Dialog目錄下的sprite名稱
   * value1 座標位置，值的內容是x,y
   * value2 淡入時間


移除sprite ``UNLOAD_SPRITE``
----------------------------------------

   * value0 sprite名稱，例如sprite_senia_01


設定立繪灰階 ``SET_GREY``
----------------------------------------

   * value0~value4 設定0~4立繪的灰階，值是0.001~1

     用0的話代表無效，所以使用接近0的值表示黑色


等候幾秒後繼續下一個對話動作 ``WAIT_SECOND``
------------------------------------------------------------

   * value0 等待時間，例如2.5秒


播放音效 ``PLAY_SOUNDFX``
------------------------------------------------------------

   播放在Resources/SoundFX的音效
 
   * value0 音效名稱


播放特效 ``SHOW_EFFECT``
------------------------------------------------------------

   播放在Resources/Dialog的特效
   
   * value0 特效名稱
   * value1 特效座標 值的內容是x,y,z


開啟CG用對話框typeB ``SHOW_MESSAGEBOX_TYPE_B``
------------------------------------------------------------

   * value0 角色名
   * value1 對話內容

關閉CG用對話框typeB ``HIDE_MESSAGEBOX_TYPE_B``
------------------------------------------------------------

   * 無參數，全部value填0


設定CG用對話框內容typeB ``SET_MESSAGEBOX_TYPE_B``
------------------------------------------------------------

   * value0 角色名
   * value1 對話內容


開啟CG用對話框type C ``SHOW_MESSAGEBOX_TYPE_C``
------------------------------------------------------------

   * value0 角色名
   * value1 對話內容

關閉CG用對話框type C ``HIDE_MESSAGEBOX_TYPE_C``
------------------------------------------------------------

   * 無參數，全部value填0

設定CG用對話框內容type C ``SET_MESSAGEBOX_TYPE_C``
------------------------------------------------------------

   * value0 角色名
   * value1 對話內容


淡入淡出黑幕 ``FADE_IN_OUT_BLACK``
------------------------------------------------------------

   * value0 淡入true, 淡出false
   * value1 淡入淡出秒數


淡入淡出白幕 ``FADE_IN_OUT_WHITE``
------------------------------------------------------------

   * value0 淡入true, 淡出false
   * value1 淡入淡出秒數


淡出全部對話 ``FADEOUT_DIALOG``
------------------------------------------------------------

   * value0 淡出秒數

