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
 
  * 測試特效時可以在編輯器Scene中使用Simulate來預覽特效，若有關閉Looping預覽會自動停止

  .. image:: /_static/image/howto-set-battleeffect/3_step.png
 
  * 在BattleEffect腳本中增加ListParticleSysytemData的Size加1
  * 新的Element將Ps欄位套用mobdie

  .. image:: /_static/image/howto-set-battleeffect/4_step.png
 
  * 將做好的特效disable
  * Save Project, Save Scene並Apply prefab再存檔


