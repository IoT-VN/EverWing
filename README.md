# EverWing
* ---------HACK KILL BOT 1 HIT-----------(Có thể chỉnh sửa tùy theo nhu cầu)

>Ctrl + F tìm this.gameStarted rồi chốt dòng }
>Dòng 72953
>Ta vào Boss Raids rồi vào Fight như bình thường sẽ bị đứng ta vào console nhập lệnh : this.bossRaidDamage = 999999999

* ---------RESET BOT -----------
>Date.prototype.getTime = function() { return 1496746800000.00 };
---------MAX CẤP ĐỘ LV 50-----------(Có thể chỉnh sửa tăng hoặc giảm cấp..)
>GC.app.mvc.commandMap.GamePlayedCommand.prototype.execute.apply({mvc :window.GC.app.mvc, finishCommand : function(e, $){}}, [{
>playerXP : 5000000,
>killedBy: null,
>secondsElapsed: null,
>playerID: null,
>background: null}
>]);
* --------Mở Khóa Toàn Bộ Nhân Vật-----------
var names = ["fiona", "sophia", "coin", "magnet", "lenore", "jade", "arcana", "lyra", "trixie"];
for (var i = 0; i < names.length; i++) {
if(GC.app.mvc.models.CharactersModel.characters[names[i]].state == "locked")
GC.app.client.runFunction("unlockCharacter",{characterName: names[i], isFree: true});
}
* --------Max Huân Chương-----------
t = GC.app.mvc.models.GameModel.trophies;
for(t; t<99999; t++){
t = t + 2000;
GC.app.mvc.commandMap.GamePlayedCommand.prototype.execute.apply({mvc :window.GC.app.mvc, finishCommand : function(e, $){}}, [{
playerXP : null,
killedBy: null,
secondsElapsed: null,
playerID: null,
background: null,
premiumEarned: 2000}
]);
}
* ---------Max Tiền-----------(Có thể tăng hoặc giảm)
GC.app.client.runFunction("addCurrency", { currency: "coins", count: 999999});
* ---------Mở Trứng Mà Không Cần Mua-----------
var amount = 10;
var sidekick = "legendary";
for(c = 0; c < amount; c++){
GC.app.client.runFunction("sidekickGacha", {isFree : true, gachaType : sidekick});
}
(Có thể thay giá trị 10>>xxx.... "legendary" ="bossraid" ....
---------HACK Max Cấp Pet----------- kèm link hướng dẫn
https://www.youtube.com/watch?v=U5-LRzzobAE&feature=youtu.be
(CTR+F) :DispatchContext.prototype.ensureNoOrphans
CODE:
var l = Object.keys(e.instances);
for (var c = 0; c < l.length; c++) {
var r = Math.floor(Math.random() * 12);
var h = e.instances[l[c]];
if(h.modelID.includes("Item:sidekick")){ 
h.stats = {maturity: 3, xp: 240000, zodiac: r, zodiacBonus: 2};
}
}
* ---------Xóa Pet Nhanh-----------kèm link hướng dẫn
https://www.youtube.com/watch?v=3qTmzZ6WdpQ&feature=youtu.be
CTR +F :onSellButtonClicked
CODE
var r = this.sidekicksModel.sidekicksList.length;
var l = Object.values(this.sidekicksModel.sidekicksList);
for (var c = 0; c < r; c++) {
var h = this.sidekicksModel.sidekicksList[c];
if(h.state === "idle"){
this.mvc.sendNotification("ReleaseSidekickCommand", h.id);
}
}
* ---------Thêm PET Vip -----------kèm link hướng dẫn
https://www.youtube.com/watch?v=Xey4f72I_NQ&feature=youtu.be
CTR+F:InstanceCache.prototype.writeDirtyInstancesToState
CODE PET VIP :
PC00 
PC22
LC38 >> Code 3 con pet cuối
HACK BẤT TỬ
https://www.youtube.com/watch?v=XtB_4o_0c1M&feature=youtu.be
CTR+F:onStartGame
CODE :
this.deathRushTimer.active = true;
this.enemies.waveSpacing = 5;
HACK ĐIỂM.....làm tương tụ như hack bất tử chỉ thay code
Ctr+F:onStartGame
CODE
this.commonEarned = 454866;
* HACK SPEED ----làm tương tụ như hack bất tử chỉ thay code
Ctr+F:onStartGame
CODE
this.enemies.enemyTier.playerSpeed = -2.5;
* HACK BẮN NHANH ----làm tương tụ như hack bất tử chỉ thay code
Ctr+F:onStartGame
CODE
this.player.shootTimeout = 0;
Hướng dẫn sử dụng: làm giống video , muốn hack gì thì coppy đoạn mã rùi Past (Ctr+V) Tìm kiếm dùng lệnh Ctr+F ...
