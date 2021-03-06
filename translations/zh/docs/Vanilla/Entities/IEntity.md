# IEntity

Entity Interface. Used to obtain and modify information entities' data.  
Entities are everything that is freely movable in the world such as players, monsters, items on the ground any many more.

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an [Array](/AdvancedFunctions/Arrays_and_Loops/)), so better be safe than sorry and add the import.  
`import crafttweaker.entity.IEntity;`

## Extending ICommandSender

IEntity extends [ICommandSender](/Vanilla/Commands/ICommandSender/). That means that all methods that are availabel to [ICommandSender](/Vanilla/Commands/ICommandSender/) Objects also are available to IEntity Objects!

<details><summary>Derived Methods</summary> 

- entity.displayName
- entity.position
- entity.world
- entity.server
- entity.sendMessage(String text)</details>

## ZenGetters

| GetterName                     | GetterMethod      | Return Type (*can be null*)                               |
| ------------------------------ | ----------------- | --------------------------------------------------------- |
| air                            | getAir()          | int                                                       |
| alive                          | isAlive()         | boolean                                                   |
| alwaysRenderNameTag            |                   | boolean                                                   |
| armorInventory                 |                   | List<[IItemStack](/Vanilla/Items/IItemStack/)             |
| canBeAttackedWithItem #可以被物体攻击 |                   | boolean                                                   |
| canBeCollidedWith #具有碰撞箱       |                   | boolean                                                   |
| canPassengerSteer #可以乘坐        |                   | boolean                                                   |
| canRiderInteract #是否可以互动       |                   | boolean                                                   |
| controllingPassenger           |                   | *IEntity*                                                 |
| customName                     | getCustomName()   | string                                                    |
| definition                     |                   | [IEntityDefinition](/Vanilla/Entities/IEntityDefinition/) |
| dimension                      | getDimension()    | int                                                       |
| doesTriggerPressurePlate       |                   | boolean                                                   |
| equipmentAndArmor              |                   | List<[IItemStack](/Vanilla/Items/IItemStack/)             |
| eyeHeight                      |                   | float                                                     |
| hasCustomName                  |                   | boolean                                                   |
| hasNoGravity                   |                   | boolean                                                   |
| heldEquipment                  |                   | List<[IItemStack](/Vanilla/Items/IItemStack/)             |
| id                             |                   | int                                                       |
| immuneToFire #免疫火焰             | isImmuneToFire()  | boolean                                                   |
| isBeingRidden                  |                   | boolean                                                   |
| isBoss                         |                   | boolean                                                   |
| isBurning                      |                   | boolean                                                   |
| isGlowing                      |                   | boolean                                                   |
| isImmuneToExplosions           |                   | boolean                                                   |
| isInLava                       |                   | boolean                                                   |
| isInsideOpaqueBlock            |                   | boolean                                                   |
| isInvisible                    |                   | boolean                                                   |
| isInvulnerable                 |                   | boolean                                                   |
| isInWater                      |                   | boolean                                                   |
| isLightningbolt                |                   | boolean                                                   |
| isOutsideBorder                |                   | boolean                                                   |
| isOverWater                    |                   | boolean                                                   |
| isPushedByWater                |                   | boolean                                                   |
| isRiding                       |                   | boolean                                                   |
| isSilent                       |                   | boolean                                                   |
| isSneaking                     |                   | boolean                                                   |
| isSprinting                    |                   | boolean                                                   |
| lowestRidingEntity             |                   | *IEntity*                                                 |
| maxFallHeight                  |                   | int                                                       |
| maxInPortalTime                |                   | int                                                       |
| onGround                       | onGround()        | boolean                                                   |
| parts                          |                   | IEntity[]                                                 |
| passengers                     | getPassengers()   | List<IEntity\>                                           |
| passengersRecursive            |                   | List<IEntity\>                                           |
| portalCooldowne                |                   | int                                                       |
| position3f                     | getPosition3f()   | [Position3f](/Vanilla/Utils/Position3f/)                  |
| ridingEntity                   | getRidingEntity() | *IEntity*                                                 |
| shouldRiderSit                 |                   | boolean                                                   |
| tags                           |                   | List<string\>                                            |
| team                           |                   | [ITeam](/Vanilla/Game/ITeam/)                             |
| wet                            | isWet()           | boolean                                                   |
| world                          |                   | [IWorld](/Vanilla/World/IWorld/)                          |
| x                              | getX()            | double                                                    |
| y                              | getY()            | double                                                    |
| z                              | getZ()            | double                                                    |
| motionX                        |                   | double                                                    |
| motionY                        |                   | double                                                    |
| motionZ                        |                   | double                                                    |
| posX                           |                   | double                                                    |
| posY                           |                   | double                                                    |
| posZ                           |                   | double                                                    |
| rotationYaw                    |                   | float                                                     |
| rotationPitch                  |                   | float                                                     |
| lookingDirection               |                   | [IVector3d](/Vanilla/World/IVector3d/)                    |
| nbt                            | getNBT()          | [IData](/Vanilla/Data/IData/)                             |

## ZenSetters

| SetterName          | SetterMethod        | 参数类型                                   |
| ------------------- | ------------------- | -------------------------------------- |
| air                 | setAir(seconds)     | int                                    |
| alwaysRenderNameTag |                     | boolean                                |
| customName          | setCustomName(name) | string                                 |
| dimension           | setDimension(id)    | int                                    |
| fire                | setFire(seconds)    | int                                    |
| hasNoGravity        |                     | boolean                                |
| id                  |                     | int                                    |
| isGlowing           |                     | boolean                                |
| isInvisible         |                     | boolean                                |
| isOutsideBorder     |                     | boolean                                |
| isSilent            |                     | boolean                                |
| isSneaking          |                     | boolean                                |
| isSprinting         |                     | boolean                                |
| position            | setPosition(pos)    | [IBlockPos](/Vanilla/World/IBlockPos/) |
| rotationYaw         |                     | float                                  |
| rotationPitch       |                     | float                                  |
| motionX             |                     | double                                 |
| motionY             |                     | double                                 |
| motionZ             |                     | double                                 |
| posX                |                     | double                                 |
| posY                |                     | double                                 |
| posZ                |                     | double                                 |
| nbt                 | setNBT()            | [IData](/Vanilla/Data/IData/)          |

## More ZenMethods

- boolean attackEntityFrom([IDamageSource](/Vanilla/Damage/IDamageSource/) source, float amount);
- boolean canTrample([IWorld](/Vanilla/World/IWorld/) world, [IBlockDefinition](/Vanilla/Blocks/IBlockDefinition/) block, [IBlockPos](/Vanilla/World/IBlockPos/) pos, float fall);
- boolean isInsideOfMaterial([IMaterial](/Vanilla/Blocks/IMaterial/) material);
- double getDistanceSqToEntity(entity); → Returns the distance to the given Entity
- [IItemStack](/Vanilla/Items/IItemStack/) getPickedResult(); → Returns the [item](/Vanilla/Items/IItemStack/) that picking up the entity would return (e.g. the item id the entity is an item or the minecart item)
- void addTag(String tag);
- void extinguish(); → Extinguishes the entity, if on fire
- void onEntityUpdate();
- void onKillCommand();
- void onUpdate();
- void removeTag(String tag);
- void setDead(); → Kills the entity
- void spawnRunningParticles();
- void removePassengers();
- void dismountRidingEntity();
- boolean isOnSameTeam(IEntity other);
- void setInWeb();
- boolean isEntityEqual(IEntity other);
- boolean isInvulnerableTo([IDamageSource](/Vanilla/Damage/IDamageSource/) source);
- boolean shouldRiderDismountInWater(IEntity rider)
- boolean boolean isPassenger(IEntity entity);
- boolean isRidingSameEntity(IEntity other);
- [IRayTraceResult](/Vanilla/World/IRayTraceResult/) getRayTrace(double blockReachDistance, float partialTicks, @Optional boolean stopOnLiquid, @Optional boolean ignoreBlockWithoutBoundingBox, @Optional(valueBoolean = true) boolean returnLastUncollidableBlock);