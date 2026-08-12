---
navigation:
  parent: example-setups/example-setups-index.md
  title: Автозаполнение интерфейса
  icon: interface
---

# Автозаполнение интерфейса

Можно задать вопрос: «Как поддерживать определённое количество различных предметов в запасе, изготавливая их по мере необходимости?»

Одно из решений — использование <ItemLink id="interface" /> (МЭ-интерфейса) и <ItemLink id="crafting_card" /> (Карты изготовления) для автоматического запроса новых предметов из системы [автоизготовления](../ae2-mechanics/autocrafting.md). Эта настройка больше подходит для поддержания небольшого количества разнообразных предметов.

Эта демонстрационная установка укорочена, чтобы не быть слишком громоздкой. Вероятно, оптимально использовать 4 <ItemLink id="interface" /> (МЭ-интерфейса) и 4 <ItemLink id="storage_bus" /> (Шины хранения), чтобы задействовать все 8 [каналов](../ae2-mechanics/channels.md) в обычном [кабеле](../items-blocks-machines/cables.md).

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/interface_autostocking.snbt" />

<BoxAnnotation color="#dddddd" min="0 0 0" max="2 1 1">
        (1) МЭ-интерфейсы: Настроены на хранение желаемых предметов в себе. Содержат Карты изготовления.
        <ItemImage id="crafting_card" scale="2" />
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="0 1 0" max="2 1.3 1">
        (2) Шины хранения: Режим ввода/вывода установлен на «Только извлечение».
  </BoxAnnotation>

<DiamondAnnotation pos="4 0.5 0.5" color="#00ff00">
        К основной сети
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Настройки

* <ItemLink id="interface" /> (МЭ-интерфейсы) (1) настроены на хранение желаемых предметов: выберите предмет в верхние слоты интерфейса или перетащите его из JEI, затем нажмите на иконку гаечного ключа над слотами, чтобы установить количество. В них установлены <ItemLink id="crafting_card" /> (Карты изготовления).
* <ItemLink id="storage_bus" /> (Шины хранения) (2) настроены так, чтобы режим ввода/вывода был установлен на «Только извлечение».

## Как это работает

1. Если <ItemLink id="interface" /> (МЭ-интерфейс) не может получить достаточно настроенного предмета из [сетевого хранилища](../ae2-mechanics/import-export-storage.md) и в нём установлена <ItemLink id="crafting_card" /> (Карта изготовления), он запросит у системы [автоизготовления](../ae2-mechanics/autocrafting.md) создание дополнительных предметов.
2. <ItemLink id="storage_bus" /> (Шины хранения) позволяют сети получать доступ к содержимому интерфейсов.