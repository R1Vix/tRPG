# tRPG

畫面布局：
	2000px * 1000px 棋盤（20 * 10 格）//這個比例看起來還是很怪，海大真的太窄長了
	1500px * 1000px 資料

遊戲角色（括號後面為詳細內容，用popup呈現）：
	模板：
		角色名稱，職業（職業敘述）
		等級（強度基準，升級可提升1個技能等級） 移動距離  HP（一旦歸零就會脫離地圖） 攻擊（數值越高，給予敵人的傷害越大） 速度（高於敵人5以上即可追擊（攻擊2次）） 防禦（防禦敵人的物理攻擊） 魔防（防禦敵人的魔法攻擊）//如果我們有加入魔防再加入這個數值，後面也是
		武器 武器攻擊距離 武器攻擊力（武器敘述與技能）
		技能1（技能1敘述）
		技能2（技能2敘述）
		技能3（技能3敘述）

	我方角色(4到6隻)：
		召喚師（主角，使用劍作為武器，能力平均)
		4 2 22(60%) 13(65%) 7(55%) 11(60%) 8(45%)
		斬裂劍 1 【6 / 10 / 14】 召喚師的御用武器，戰鬥中的攻擊與防禦 + 7
		至尊召喚師（當自己的HP高於2，且受到敵人致命攻擊時，將傷害盡低至身HP會剩下1，）
		反擊（【若自身HP為100%， / 若自身HP高於50%， /】受到敵人攻擊時，可無視距離進行反擊）
		痊癒（【奇數回合開始時，回復4HP / 回合開始時，回復4HP / 回合開始時，回復7HP】）

		重裝兵（使用斧頭作為武器，擁有優秀的防禦力，但移動速度較慢）
		1 2 25(70%) 11(65%) 6(50%) 12(65%) 5(40%)
		防守隊形（若自身HP高於【75% / 50% / 25%】時，自己與敵人皆無法進行追擊）

		騎兵（使用槍作為武器，機動性極高）
		1 3 21(45%) 9(50%) 8(45%) 9(45%) 12(60%)
		衝敵斬（由自己發動攻擊時，戰鬥後，替換自己和敵人的位置）
		回擊（受到敵人攻擊時，若自身HP高於【75% / 50% / 25% / 】時，則必定可進行追擊）
		麗華(受到敵人攻擊時，戰鬥中的魔防 +【2 / 4 / 7】)
		疾風迅雷(移動+1)

		弓箭手（使用弓作為武器，射程2）
		1 2 19(55%) 9(60%) 8(65%) 7(50%) 6(35%)
		覺醒(由自己發動攻擊時，戰鬥中的速度+【2 / 4 / 7】)
		蛇毒(由自己發動攻擊時，戰鬥後給予敵人【4 / 7 / 10】傷害)

		//如果我們有加入魔防再加入這個角色
		魔刃（使用黑魔法作為武器，以敵人的魔防計算傷害）
		1 2 19(55%) 8(55%) 8(55%) 8(55%) 6(45%)
		冰河(由自己發動攻擊時，戰鬥中的攻擊增加自身魔防的【30% / 50% / 80%】)

		//如果我們有加入輔助技再加入這個角色
		僧侶（使用白魔法作為武器，可以輔助我方單位）
		1 2 19(60%) 6(50%) 7(45%) 6(45%) 11(65%)
		治癒(回復【5 / 10 / 攻擊的50%】HP)
		奉獻(回復我方時，自己也會回復其回復量的【50% / 75% / 100%】)

	敵方角色（15到20隻，）：
		默靈頭目 * 1，盜賊（使用劍作為武器，能力優秀)
		始祖斬裂劍 1 【6 / 10 / 14】 默靈的專屬武器，，攻擊時，攻擊2次（被敵人攻擊時也可以攻擊2次）
		【5 0 23 10 12 11 9 / 8 0 25 13 14 12 10 / 10 0 27 15 16 14 13】
		反擊（受到敵人攻擊時，可無視距離進行反擊）

		默靈刺客 * 3（使用劍作為武器，能力平均)
		【4 / 6 / 9 2 20(60%) 10(65%) 7(55%) 8(60%) 6(45%)】
		
		默靈重裝兵 * 4（使用斧頭作為武器，擁有優秀的防禦力，但移動速度較慢）
		【4 / 6 / 9 1 23(65%) 10(65%) 6(50%) 13(60%) 7(55%)】
		
		默靈騎兵 * 4（使用槍作為武器，機動性極高）
		【4 / 6 / 9 3 22(55%) 10(60%) 10(50%) 7(50%) 7(50%)】
		
		默靈弓箭手 * 3（使用弓作為武器，可以攻擊較遠的敵人）
		【4 / 6 / 9 2 19(50%) 7(50%) 9(65%) 5(40%) 9(65%)】
		
		//如果我們有加入魔防再加入這兩個角色
		默靈魔刃 * 3（使用黑魔法作為武器，以敵人的魔防計算傷害）
		【4 / 6 / 9 2 20(65%) 7(45%) 6(50%) 9(60%) 7(50%)】
		
		//如果我們有加入輔助技再加入這個角色
		默靈僧侶 * 2（使用白魔法作為武器，可以輔助我方單位）
		【4 / 6 / 9 0 22(55%) 9(65%) 12(75%) 7(50%) 9(75%)】

遊戲流程：
	打開網站
	> 檢查有沒有歷史紀錄，若有則載入
	> 選擇難度
	載入背景故事，一共三張全屏圖案：

		在不久後的未來，隨著科技的發展，人類能夠自由分離並控制自己的靈魂，而精通這項技術的人，在當時則稱作「召喚師」。但是在召喚過程中，若操作不當，很可能會使靈魂與肉體徹底分離，形成所謂的「默靈」。默靈會侵蝕人類，並將其肉體佔為己有，唯有召喚師才能徹底消滅默靈。


		「啊啊啊啊啊！」「竟然睡過頭！」
		「開學第一天就要遲到了啦！！怎麼辦！！！」

		我，是一位大學新鮮人，別看我一臉呆樣，其實我是一位召喚師，
		雖然我的能力尚未成熟，但我相信在接下來的大學生活中一定會派上用場的！」


		「欸？奇怪？明明今天開學，怎麼學校一個人都沒有？
		「救命啊！默靈入侵校園內了啦！」怎麼會這樣？
		「好像是被海浪拍上岸的，現在校園內全部都是默靈！」
		怎麼可以開學第一天就這樣！
		雖然我能力有限，但是這些數量，我應該能夠應付的吧！」

	//看看這裡要不要放個教學，跟背景故事放一起
	
	遊戲開始
	戰鬥目標：打倒默靈頭目
	
	我方回合

	初始化我方角色的數值與狀態（可以行動True）
	執行「回合開始」類型的技能
	當點選我方角色時，角色背景變成深藍色，角色可移動的範圍背景變成淺藍色，角色可移動的範圍內可攻擊的格子和的敵人背景變成紅色
	選擇我方角色要移動到的目標，這時候角色的圖案應該要跟著移動
	選擇我方角色要攻擊的目標，執行「戰鬥時」類型的技能並顯示戰鬥預測函式
	再一次點選攻擊目標，攻擊，跑攻擊動畫
	根據攻擊結果「戰鬥後」類型的技能
	可以行動False，可以行動的單位人數 - 1
	重複直到可以行動的單位人數 = 0
	
	敵方回合
	初始化敵方角色的數值與狀態（可以行動True）
	執行「回合開始」類型的技能
	從敵方單位的ID一個一個跑，選擇攻擊對象（優先順序：戰勝、維持、戰敗），若沒有對象則可以行動False，
	跑每一個角色的攻擊動畫

第一階段
	棋盤與點選棋格函式
	美術
第二階段
	數值與技能實裝
	戰鬥預測函式
	敵方回合行動函式
第三階段
	動畫
	Cookies
第四階段
	後端？？？