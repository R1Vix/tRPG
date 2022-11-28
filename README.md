# tRPG

畫面布局：
	2000px * 1000px 棋盤（20 * 10 格）
	1500px * 1000px 資料

遊戲角色（括號後面為詳細內容，用popup呈現）：
	模板：
		角色名稱，職業（職業敘述）
		等級（強度基準，升級可提升1個技能等級） HP（一旦歸零就會脫離地圖） 攻擊（數值越高，給予敵人的傷害越大） 速度（高於敵人5以上即可追擊（攻擊2次）） 防禦（防禦敵人的物理攻擊） 魔防（防禦敵人的魔法攻擊）
		技能1（技能1敘述）
		技能2（技能2敘述）
		技能3（技能3敘述）

	我方角色(4到6隻)：
		召喚師（主角，使用劍作為武器，能力平均)
		4 22(60%) 13(65%) 7(55%) 11(60%) 8(45%)
		至尊召喚師（當自己的HP高於2，且受到敵人致命攻擊時，將傷害盡低至身HP會剩下1，）
		反擊（【若自身HP為100%， / 若自身HP高於50%， /】受到敵人攻擊時，可無視距離進行反擊）
		痊癒（【奇數回合開始時，回復4HP / 回合開始時，回復4HP / 回合開始時，回復7HP】）

		重裝兵（使用斧頭作為武器，擁有優秀的防禦力，但移動速度較慢）
		1 25(70%) 11(65%) 6(50%) 12(65%) 5(40%)
		防守隊形（若自身HP高於【75% / 50% / 25%】時，自己與敵人皆無法進行追擊）

		騎兵（使用槍作為武器，機動性極高）
		1 21(45%) 9(50%) 8(45%) 9(45%) 12(60%)
		衝敵斬（由自己發動攻擊時，戰鬥後，替換自己和敵人的位置）
		回擊（受到敵人攻擊時，若自身HP高於【75% / 50% / 25%】時，則必定可進行追擊）
		
		弓箭手（使用弓作為武器，射程2）
		1 19(55%) 9(60%) 8(65%) 7(50%) 6(35%)\
		覺醒(由自己發動攻擊時，戰鬥中的攻擊+【2 / 4 / 7】)
		蛇毒(由自己發動攻擊時，戰鬥後給予敵人【4 / 7 / 10】傷害)
		
		//如果我們有加入魔防再加入這個角色
		魔刃（使用黑魔法作為武器，以敵人的魔防計算傷害）
		1 19(55%) 8(55%) 8(55%) 8(55%) 6(45%)
		冰河(由自己發動攻擊時，戰鬥中的攻擊增加自身魔防的【30% / 50% / 80%】)
		
		//如果我們有加入輔助技再加入這個角色
		僧侶（使用白魔法作為武器，可以輔助我方單位）
		1 19(60%) 6(50%) 7(45%) 6(45%) 11(65%)
		治癒(回復【5 / 10 / 攻擊的50%】HP)
		奉獻(回復我方時，自己也會回復其回復量的【50% / 75% / 100%】)

	敵方角色（15到20隻，）：
		盜賊頭目 * 1，盜賊（使用劍作為武器，能力優秀)
		【5 23 10 12 11 9 / 8 25 13 14 12 10 / 10 27 15 16 14 13】
		反擊（受到敵人攻擊時，可無視距離進行反擊）

		刺客 * 3（使用劍作為武器，能力平均)
		【4 / 6 / 8】
		
		重裝兵 * 4（使用斧頭作為武器，擁有優秀的防禦力，但移動速度較慢）
		【4 / 6 / 8】
		
		騎兵 * 4（使用槍作為武器，機動性極高）
		【4 / 6 / 8】
		
		弓箭手 * 3（使用弓作為武器，可以攻擊較遠的敵人）
		【4 / 6 / 8】
		
		//如果我們有加入魔防再加入這兩個角色
		魔刃 * 3（使用黑魔法作為武器，以敵人的魔防計算傷害）
		【4 / 6 / 8】
		
		//如果我們有加入輔助技再加入這個角色
		僧侶 * 2（使用白魔法作為武器，可以輔助我方單位）
		【4 / 6 / 8】

遊戲流程：
	打開網站
	> 檢查有沒有歷史紀錄，若有則載入
	> 選擇難度

遊戲規則

第一階段
第二階段
第三階段
