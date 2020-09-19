# PlayerAnvilRepair

The PlayerAnvilRepair Event is fired whenever a player crafts something in the anvil.  
You can change the chance that the anvil is damaged.

## Event Class

You will need to cast the event in the function header as this class:  
`crafttweaker.event.PlayerAnvilRepairEvent`  
You can, of course, also [import](/AdvancedFunctions/Import/) the class before and use that name then.

## Event interface extensions

PlayerAnvilRepair Events implement the following interfaces and are able to call all of their methods/getters/setters as well:

- [IPlayerEvent](/Vanilla/Events/Events/IPlayerEvent/)

## ZenGetters

다음 정보들은 이벤트를 통해서 얻을 수 있습니다.

| ZenGetter        | ZenSetter     | 반환 타입                                    |
| ---------------- | ------------- | ---------------------------------------- |
| `player`         |               | [IPlayer](/Vanilla/Players/IPlayer/)     |
| `itemInput`      |               | [IItemStack](/Vanilla/Items/IItemStack/) |
| `itemIngredient` |               | [IItemStack](/Vanilla/Items/IItemStack/) |
| `itenResult`     |               | [IItemStack](/Vanilla/Items/IItemStack/) |
| `breakChance`    | `breakChance` | float                                    |