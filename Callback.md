## ？
Callback.addCallback("ReadSaves", function(globalScope){
});
## ？
Callback.addCallback("WriteSaves", function(globalScope){
});
## ？
Callback.addCallback("CustomBlockTessellation", function(api, coords, block, b){
});
## 読み込み直前
Callback.addCallback("PreLoaded", function(){
});
## APIが読み込まれた時
Callback.addCallback("APILoaded", function(){
});
## Modが読み込まれた時
Callback.addCallback("ModsLoaded", function(){
});
## Postが読み込まれた時？
Callback.addCallback("PostLoaded", function(){
});
## ？
Callback.addCallback("AppSuspended", function(){
});
## Levelを選択時
Callback.addCallback("LevelSelected", function(worldName, worldDir){
});
## Levelの読み込み直前
Callback.addCallback("LevelPreLoaded", function(){
});
## Levelが読み込まれた時
Callback.addCallback("LevelLoaded", function(){
});
## 次元(オーバーワールド、ネザー、エンド)が読み込まれた時
Callback.addCallback("DimensionLoaded", function(dimension){
});
## Levelを去る直前
Callback.addCallback("LevelPreLeft", function(){
});
## Levelを去った時
Callback.addCallback("LevelLeft", function(){
});
## Blockの破壊時
Callback.addCallback("DestroyBlock", function(Coords, Block, Player){
});
## Blockの破壊開始時
Callback.addCallback("DestroyBlockStart", function(Coords, Block, Player){
});
## Block設置時
Callback.addCallback("BuildBlock", function(Coords, Block, Player){
});
## Item使用時
Callback.addCallback("ItemUse", function(coords, Item, Block){
});
## 爆発発生時
Callback.addCallback("Explosion", function(objArr){
});
## 食べた時
Callback.addCallback("FoodEaten", function(food,ratio){
});
## 経験値追加時
Callback.addCallback("ExpAdd", function(exp){
});
## レベルアップ時
Callback.addCallback("ExpLevelAdd", function(level){
});
## コマンド実行時
Callback.addCallback("NativeCommand", function(objArr){
});
## Player攻撃時
Callback.addCallback("PlayerAttack", function(attacker, entity){
});
##
Callback.addCallback("EntityInteract", function(entity, player){
});
## Entity削除時
Callback.addCallback("EntityRemoved", function(entity){
});
## Entity死亡時
Callback.addCallback("EntityDeath", function(entity, attacker,damageType){
});
## 弓矢などのProjectileが当たった時
Callback.addCallback("ProjectileHit", function(objArr){
});
## レッドストーンの？？時
Callback.addCallback("RedstoneSignal", function(r8){
});
## Itemのアイコン上書き時
Callback.addCallback("ItemIconOverride", function(Item){
});
## Item名上書き時
Callback.addCallback("ItemNameOverride", function(Item, translated, name){
});
## ターゲットなしにアイテム使用時
Callback.addCallback("ItemUseNoTarget", function(Item){
});
## Itemのリリース時
Callback.addCallback("ItemUsingReleased", function(Item, ticks){
});
## Itemの使用完了時
Callback.addCallback("ItemUsingComplete", function(Item){
});
## Itemが発射?された時
Callback.addCallback("ItemDispensed", function(Coords, Item){
});
## ネイティブのUIに変更があった時
Callback.addCallback("NativeGuiChanged", function(name){
});
##
Callback.addCallback("PreBlocksDefined", function(){
});
##
Callback.addCallback("BlocksDefined", function(){
});
## 1/20s毎
Callback.addCallback("tick",function(){
});
## チャンク成形時
Callback.addCallback("GenerateChunk", function(chunkX, chunkZ){
});
## アンダーグラウンドでチャンク成形時
Callback.addCallback("GenerateChunkUnderground", function(chunkX, chunkZ){
});
## ネザーのチャンク成形時
Callback.addCallback("GenerateNetherChunk", function(chunkX, chunkZ){
});
## エンドのチャンク成形時
Callback.addCallback("GenerateEndChunk", function(chunkX, chunkZ){
});
