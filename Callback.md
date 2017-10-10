Callback.addCallback("ReadSaves", function(globalScope){
});

Callback.addCallback("WriteSaves", function(globalScope){
});

Callback.addCallback("CustomBlockTessellation", function(api, coords, block, b){
});

Callback.addCallback("PreLoaded", function(){
});

Callback.addCallback("APILoaded", function(){
});

Callback.addCallback("ModsLoaded", function(){
});

Callback.addCallback("PostLoaded", function(){
});

Callback.addCallback("AppSuspended", function(){
});

Callback.addCallback("LevelSelected", function(worldName, worldDir){
});

Callback.addCallback("LevelPreLoaded", function(){
});

Callback.addCallback("LevelLoaded", function(){
});

Callback.addCallback("DimensionLoaded", function(dimension){
});

Callback.addCallback("LevelPreLeft", function(){
});

Callback.addCallback("LevelLeft", function(){
});

Callback.addCallback("DestroyBlock", function(Coords, Block, Player){
});

Callback.addCallback("DestroyBlockStart", function(Coords, Block, Player){
});

Callback.addCallback("BuildBlock", function(Coords, Block, Player){
});

Callback.addCallback("ItemUse", function(coords, Item, Block){
});

Callback.addCallback("Explosion", function(objArr){
});

Callback.addCallback("FoodEaten", function(food,ratio){
});

Callback.addCallback("ExpAdd", function(exp){
});

Callback.addCallback("ExpLevelAdd", function(level){
});

Callback.addCallback("NativeCommand", function(objArr){
});

Callback.addCallback("PlayerAttack", function(attacker, entity){
});

Callback.addCallback("EntityInteract", function(entity, player){
});

Callback.addCallback("EntityRemoved", function(entity){
});

Callback.addCallback("EntityDeath", function(entity, attacker,damageType){
});

Callback.addCallback("ProjectileHit", function(objArr){
});

Callback.addCallback("RedstoneSignal", function(r8){
});

Callback.addCallback("ItemIconOverride", function(Item){
});

Callback.addCallback("ItemNameOverride", function(Item, translated, name){
});

Callback.addCallback("ItemUseNoTarget", function(Item){
});

Callback.addCallback("ItemUsingReleased", function(Item, ticks){
});

Callback.addCallback("ItemUsingComplete", function(Item){
});

Callback.addCallback("ItemDispensed", function(Coords, Item){
});

Callback.addCallback("NativeGuiChanged", function(name){
});

Callback.addCallback("PreBlocksDefined", function(){
});

Callback.addCallback("BlocksDefined", function(){
});

Callback.addCallback("tick",function(){
});

Callback.addCallback("GenerateChunk", function(chunkX, chunkZ){
});

Callback.addCallback("GenerateChunkUnderground", function(chunkX, chunkZ){
});

Callback.addCallback("GenerateNetherChunk", function(chunkX, chunkZ){
});

Callback.addCallback("GenerateEndChunk", function(chunkX, chunkZ){
});
