Callback.invokeAPICallback("PreLoaded", new Object[0]);

Callback.invokeAPICallback("APILoaded", new Object[0]);

Callback.invokeAPICallback("ModsLoaded", new Object[0]);

Callback.invokeAPICallback("PostLoaded", new Object[0]);

Callback.invokeAPICallback("AppSuspended", new Object[0]);

Callback.invokeAPICallback("LevelSelected", worldName, worldDir);

Callback.invokeAPICallback("LevelPreLoaded", new Object[0]);

Callback.invokeAPICallback("LevelLoaded", new Object[0]); 

Callback.invokeAPICallback("DimensionLoaded", Integer.valueOf(dimension));

Callback.invokeAPICallback("LevelPreLeft", new Object[0]);

Callback.invokeAPICallback("LevelLeft", new Object[0]);   

Callback.invokeAPICallback("DestroyBlock", new Coords(x, y, z, side), new FullBlock(NativeAPI.getTileAndData(x, y, z)), Long.valueOf(NativeAPI.getPlayer()));
     
Callback.invokeAPICallback("DestroyBlockStart", new Coords(x, y, z, side), new FullBlock(NativeAPI.getTileAndData(x, y, z)), Long.valueOf(NativeAPI.getPlayer()));

Callback.invokeAPICallback("DestroyBlockContinue", new Coords(x, y, z, side), new FullBlock(NativeAPI.getTileAndData(x, y, z)), Long.valueOf(NativeAPI.getPlayer()));

Callback.invokeAPICallback("BuildBlock", new Coords(x, y, z, side), new FullBlock(NativeAPI.getTileAndData(x, y, z)), Long.valueOf(NativeAPI.getPlayer()));

Callback.invokeAPICallback("ItemUse", coords, new ItemInstance(NativeAPI.getEntityCarriedItem(NativeAPI.getPlayer()));

Callback.invokeAPICallback("Explosion", objArr);

Callback.invokeAPICallback("FoodEaten", Integer.valueOf(food), Float.valueOf(ratio));

Callback.invokeAPICallback("ExpAdd", Integer.valueOf(exp));

Callback.invokeAPICallback("ExpLevelAdd", Integer.valueOf(level));

Callback.invokeAPICallback("NativeCommand" , objArr);

Callback.invokeAPICallback("PlayerAttack", Long.valueOf(attacker), Long.valueOf(entity));

Callback.invokeAPICallback("EntityInteract", Long.valueOf(entity), Long.valueOf(player));

Callback.invokeAPICallback("EntityAdded", Long.valueOf(entity));

Callback.invokeAPICallback("EntityRemoved", Long.valueOf(entity));

Callback.invokeAPICallback("EntityDeath", Long.valueOf(entity), Long.valueOf(attacker), Integer.valueOf(damageType));

Callback.invokeAPICallback("EntityHurt", Long.valueOf(attacker), Long.valueOf(entity), Integer.valueOf(damageValue), Integer.valueOf(damageType), Boolean.valueOf(someBool1), Boolean.valueOf(someBool2));

Callback.invokeAPICallback("ProjectileHit", objArr);

Callback.invokeAPICallback("RedstoneSignal", r8);

Callback.invokeAPICallback("ItemIconOverride", new ItemInstance(id, count, data));

Callback.invokeAPICallback("ItemNameOverride", new ItemInstance(id, count, data), translated, name);

Callback.invokeAPICallback("ItemUseNoTarget", new ItemInstance(NativeAPI.getEntityCarriedItem(NativeAPI.getPlayer())));

Callback.invokeAPICallback("ItemUsingReleased", new ItemInstance(NativeAPI.getEntityCarriedItem(NativeAPI.getPlayer())), Integer.valueOf(ticks));

Callback.invokeAPICallback("ItemUsingComplete", new ItemInstance(NativeAPI.getEntityCarriedItem(NativeAPI.getPlayer())));

Callback.invokeAPICallback("ItemDispensed", new Coords((double) x, (double) y, (double) z).setSide(side), new ItemInstance(id, count, data));

Callback.invokeAPICallback("NativeGuiChanged", "screen_name");
