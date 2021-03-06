# ICommandSender

Интерфейс ICommandSender используется в качестве основы для всех сущностей и еще нескольких типов CraftTweaker.  
Каждый объект [IEntity](/Vanilla/Entities/IEntity/) и [IPlayer](/Vanilla/Players/IPlayer/) реализует этот интерфейс!

## Импорт пакета

Может потребоваться импортировать пакет, если вы обнаруживаете какие-либо проблемы (вроде приведения типа [массива](/AdvancedFunctions/Arrays_and_Loops/)), поэтому в качестве меры предосторожности лучше добавить импорт:  
`import crafttweaker.command.ICommandSender;`

## Геттеры

| Геттер      | Возвращаемый тип                       |
| ----------- | -------------------------------------- |
| displayName | string                                 |
| position    | [IBlockPos](/Vanilla/World/IBlockPos/) |
| world       | [IWorld](/Vanilla/World/IWorld/)       |
| server      | [IServer](/Vanilla/Game/IServer/)      |

## Методы

### Send Message

Takes a String Returns void (nothing).

```zenscript
sender.sendMessage(String text);
```

### Send Rich Text Message

Takes an [ITextComponent](/Vanilla/Text/ITextComponent/) Returns void (nothing).

```zenscript
sender.sendRichTextMessage(ITextComponent textComponent);
```