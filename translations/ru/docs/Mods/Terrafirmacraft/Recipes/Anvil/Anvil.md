# Наковальня

## Пакет
```zenscript
import mods.terrafirmacraft.наковальня;
```

## Сложение

```zenscript
Anvil.addRecipe(String registryName, IIngredient input, IItemStack output, int minTier, String skillType, String... forgeRules);
```
- Вход не может быть скопирован. Безьялы принимают только по одному предмету за слот.
- ввод должен быть форгелируемым (обратитесь к [ItemRegistry](/Mods/Terrafirmacraft/ItemRegistry) для регистрации возможности ковки предмета).
- Ранг равен 0 = камень, 1 = медь, 2 = бронза, 3 = засушливое железо, 4 = Сталь, 5 = Черная Сталь и 6 = Красная/Синяя Сталь.
- Тип навыка - какая категория навыка должна участвовать в ковке. Допустимые записи `общие`, `инструменты`, `оружие`, `броня`, или null. Если тип навыка `инструменты`, `оружия`, или `броня` , то в результате предмету будет применен бонус к навыку.
- Рецепт должен иметь 1, 2 или 3 правила. Правила состоят из типа (`HIT`, `DRAW`, `НАЧАЛО`, `ОТПРАВКА`, `ОБСМОТР`или `СЧРИНК`), следовал заказ (`ЛЮБОЙ`, `NOT_LAST`, `ПОСЛЕДНИЙ`, `SECOND_LAST`, `THIRD_LAST`), разделенные подчеркиванием. Например, `HIT_ANY`, `DRAW_SECOND_LAST`и `UPSET_NOT_LAST` являются допустимыми именами правил.

## Удаление

```zenscript
Anvil.removeRecipe(IItemStack);
Anvil.removeRecipe(String registryName);
```