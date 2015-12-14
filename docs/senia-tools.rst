專案工具
========================================


SeniaPlayerData Editor
----------------------------------------

SeniaPlayerData Editor可用來修改玩家和角色資料

.. warning:: 不要在遊戲中啟動時同時修改資料，會導致資料錯誤

開啟編輯器，可將視窗拖曳至Unity的邊緣固定
   .. image:: /_static/image/senia-tools/1_seniaplayerdataeditor_0.png
   
   
Player分頁
   .. image:: /_static/image/senia-tools/1_seniaplayerdataeditor_1.png
   
   * Delete PlayerPrefs 刪除玩家和角色資料
   * Revert PlayerPrefs 還原目前正在修改的資料
   * Save PlayerPrefs 將目前修改的資料存至本機
      
   * PlayerID 玩家ID，未來可能使用平台的ID
   * Coin 玩家金錢，目前不使用
   * SP 玩家SP
   * IsCheater 此玩家是否作弊過
   * CurrentCharacterID 玩家目前使用的角色ID
   * CurrentBattleLevel 玩家目前關卡進度，必須要一次加5關，例如1、6、11、...
   * ListReadedStoryID 已讀的劇情ID

Character分頁
   .. image:: /_static/image/senia-tools/1_seniaplayerdataeditor_2.png
   
   * CharacterID 選擇要修改的角色ID來修改
   * Level 角色等級
   * statsPoint 屬性配點
   * Exp 經驗值
   * Mp 魔力
   * CurrentSkillQ 目前設定技能的ID(目前固定)
   * CurrentSkillW 目前設定技能的ID(目前固定)

   * str1 角色屬性
   * agi1 角色屬性
   * int1 角色屬性
   * dex1 角色屬性
   * luk1 角色屬性

   * SkillLv 技能等級，skillid XX與表格skillclass.csv相同
   
表格轉換工具
----------------------------------------
