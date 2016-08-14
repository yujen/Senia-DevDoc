設定戰鬥特效
========================================


戰鬥的特效放在Battle場景的BattleEffect，以mobdie特效為例設定

  .. image:: /_static/image/howto-set-battleeffect/0_step.png
 
  * 將特效放在BattleEffect prefab下
  * Duration 特效播放時間，盡量接近實際長度減少空特效時間
  * 若特效只播一次則關閉Looping

  .. image:: /_static/image/howto-set-battleeffect/1_step.png
 
  * AutoDestroyGameObject腳本開啟Only Disable讓特效播放結束時自動關閉
  * Shader使用Mobile/Particles底下的版本
  
  .. image:: /_static/image/howto-set-battleeffect/2_step.png
 
  * 將做好的特效disable
  * Save Project, Save Scene並Apply prefab再存檔


