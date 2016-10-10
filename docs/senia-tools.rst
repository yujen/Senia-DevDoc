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
   * ListEquipData 玩家擁有的裝備資料，將Count增加會自動在列表後方加入新的裝備資料
   
     - uid 裝備的唯一辨識id，不可重複
     - id 裝備id，對照至weapon.csv的id
     - level 裝備等級


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
   
   * CurrentEquipList 目前角色所裝備的裝備，最大五格位置，uid必須要在玩家ListEquipData中


  
表格測試工具
----------------------------------------

SeniaTableUnitTest Editor可用來測試表格機率是否正確

  dropgroup.csv
   .. image:: /_static/image/senia-tools/2_SeniaTableUnitTest_Editor.png
   
   * TableName 選擇要測試的表格
   * DropGroupId 要測試的id
   * TestCount 測試次數
   
   按下Start Test後會在下方顯示測試後的資訊，Probability表示怪物掉落物品機率


表格轉換工具
----------------------------------------

"Menu > Senia > Convert CSV to JSON"

  * 可以把Table/目錄下的csv檔轉成遊戲用的json格式
  * 可以在csv檔開啟編輯中直接進行轉換
  * 要build遊戲前要先執行這個工具


怪物prefab複製工具
----------------------------------------

"Menu > Senia > SeniaMobPrefab Editor"
  
  .. image:: /_static/image/senia-tools/3_SeniaMobPrefab_Editor.png

  * 將想要複製的怪物prefab拖曳到"來源怪物prefab"
  * 輸入新怪物ID，小心不要有重複
  * 將需要共用的動畫打勾，會共用來源怪物的動畫
  * 複製Prefab按鈕，會複製整個怪物的script/動畫/圖檔資源，並放在相對應的新怪物ID目錄下

