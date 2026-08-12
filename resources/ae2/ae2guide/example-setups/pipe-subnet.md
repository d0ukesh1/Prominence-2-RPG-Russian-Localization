---
navigation:
  parent: example-setups/example-setups-index.md
  title: Подсеть "Труба" для предметов/жидкостей
  icon: storage_bus
---

# Подсеть "Труба" для предметов/жидкостей

Простой способ эмуляции трубы для предметов и/или жидкостей с использованием [устройств](../ae2-mechanics/devices.md) мода Applied Energistics 2, полезный для любых задач, где обычно используются трубы для предметов или жидкостей.
Это включает возврат результатов крафта в <ItemLink id="pattern_provider" /> (МЭ поставщик шаблонов).

Существует два основных метода реализации этого:

## Шина импорта -> Шина хранения

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/import_storage_pipe.snbt" />

<BoxAnnotation color="#dddddd" min="3.7 0 0" max="4 1 1">
        (1) Шина импорта: Можно настроить фильтр.
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="1 0 0" max="1.3 1 1">
        (2) Шина хранения: Можно настроить фильтр. Эта (и другие шины хранения, которые вы хотите использовать как пункт назначения)
        должна быть единственным хранилищем в сети.
  </BoxAnnotation>

<DiamondAnnotation pos="4.5 0.5 0.5" color="#00ff00">
        Источник
    </DiamondAnnotation>

<DiamondAnnotation pos="0.5 0.5 0.5" color="#00ff00">
        Пункт назначения
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<ItemLink id="import_bus" /> (МЭ шина импорта) (1) на исходном инвентаре импортирует предметы или жидкости и пытается сохранить их в [сетевом хранилище](../ae2-mechanics/import-export-storage.md).
Поскольку единственным хранилищем в сети является <ItemLink id="storage_bus" /> (МЭ шина хранения) (2) (поэтому это подсеть, а не основная сеть), предметы или жидкости
помещаются в инвентарь пункта назначения, таким образом передаваясь. Энергия подаётся через <ItemLink id="quartz_fiber" /> (Кварцевое волокно).
И шина импорта, и шина хранения могут быть отфильтрованы, но если фильтры не установлены, система будет передавать всё, к чему имеет доступ.
Эта схема также работает с несколькими шинами импорта и несколькими шинами хранения.

## Шина хранения -> Шина экспорта

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/storage_export_pipe.snbt" />

<BoxAnnotation color="#dddddd" min="3.7 0 0" max="4 1 1">
        (1) Шина хранения: Можно настроить фильтр. Эта (и другие шины хранения, которые вы хотите использовать как источник)
        должна быть единственным хранилищем в сети.
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="1 0 0" max="1.3 1 1">
        (2) Шина экспорта: Должна быть отфильтрована.
  </BoxAnnotation>

<DiamondAnnotation pos="4.5 0.5 0.5" color="#00ff00">
        Источник
    </DiamondAnnotation>

<DiamondAnnotation pos="0.5 0.5 0.5" color="#00ff00">
        Пункт назначения
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<ItemLink id="export_bus" /> (МЭ шина экспорта) на инвентаре пункта назначения пытается извлечь предметы, указанные в её фильтре, из [сетевого хранилища](../ae2-mechanics/import-export-storage.md).
Поскольку единственным хранилищем в сети является <ItemLink id="storage_bus" /> (МЭ шина хранения) (поэтому это подсеть, а не основная сеть), предметы или жидкости
извлекаются из инвентаря источника, таким образом передаваясь. Энергия подаётся через <ItemLink id="quartz_fiber" /> (Кварцевое волокно).
Поскольку шина экспорта должна быть отфильтрована для работы, эта схема функционирует только при наличии фильтра на шине экспорта.
Эта схема также работает с несколькими шинами хранения и несколькими шинами экспорта.

## Схема, которая не работает (Шина импорта -> Шина экспорта)

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/import_export_pipe.snbt" />

<BoxAnnotation color="#dd3333" min="3.7 0 0" max="4 1 1">
        Шина импорта: Поскольку в сети нет хранилища, некуда импортировать.
  </BoxAnnotation>

<BoxAnnotation color="#dd3333" min="1 0 0" max="1.3 1 1">
        (2) Шина экспорта: Поскольку в сети нет хранилища, нечего экспортировать.
  </BoxAnnotation>

<DiamondAnnotation pos="4.5 0.5 0.5" color="#ff0000">
        Источник
    </DiamondAnnotation>

<DiamondAnnotation pos="0.5 0.5 0.5" color="#ff0000">
        Пункт назначения
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Схема с использованием только шины импорта и шины экспорта не работает. Шина импорта пытается извлечь предметы из инвентаря источника
и сохранить их в сетевом хранилище. Шина экспорта пытается извлечь предметы из сетевого хранилища и поместить их
в инвентарь пункта назначения. Однако, поскольку в этой сети **нет хранилища**, шина импорта не может импортировать,
а шина экспорта не может экспортировать, поэтому ничего не происходит.

## Ввод и вывод через одну сторону

Предположим, у вас есть машина, которая может принимать входные данные и выдавать результат через одну сторону (например, <ItemLink id="charger" /> (Зарядник)).
Вы можете одновременно подавать ингредиенты и извлекать результат, комбинируя два метода подсети-трубы:

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/import_storage_export_pipe.snbt" />

<BoxAnnotation color="#dddddd" min="4 1 1" max="5 1.3 2">
        (1) Шина импорта: Можно настроить фильтр.
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="2 1 1" max="3 1.3 2">
        (2) Шина хранения: Можно настроить фильтр. Эта (и другие шины хранения, которые вы хотите использовать для ввода и вывода предметов)
        должна быть единственным хранилищем в сети.
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="2 0 1" max="3 1 2">
        (3) Объект, в который вы хотите подавать и из которого извлекать: В данном случае Зарядник.
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="0 1 1" max="1 1.3 2">
        (4) Шина экспорта: Должна быть отфильтрована.
  </BoxAnnotation>

<DiamondAnnotation pos="4.5 0.5 1.5" color="#00ff00">
        Источник
    </DiamondAnnotation>

<DiamondAnnotation pos="0.5 0.5 1.5" color="#00ff00">
        Пункт назначения
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Интерфейсы

Оказывается, существуют [устройства](../ae2-mechanics/devices.md), помимо шин импорта и экспорта, которые могут помещать предметы в
и извлекать их из [сетевого хранилища](../ae2-mechanics/import-export-storage.md)!
В данном случае важен <ItemLink id="interface" /> (МЭ-интерфейс). Если в интерфейс помещается предмет, который не настроен для хранения, интерфейс
передаёт его в сетевое хранилище, что мы можем использовать аналогично схеме шина импорта -> шина хранения. Настройка интерфейса на
хранение определённых предметов позволяет извлекать их из сетевого хранилища, подобно схеме шина хранения -> шина экспорта. Интерфейсы могут быть настроены
на хранение одних предметов и не хранение других, что позволяет удалённо подавать и извлекать через шины хранения, если это по какой-то причине нужно.

<GameScene zoom="6" background="transparent">
<ImportStructure src="../assets/assemblies/interface_pipes.snbt" />

<BoxAnnotation color="#dddddd" min="3.7 0 0" max="4 1 1">
        МЭ-интерфейс
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="1 0 0" max="1.3 1 1">
        Шина хранения
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="3.7 0 2" max="4 1 3">
        Шина хранения
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="0 1 2" max="1 1.3 3">
        Шина хранения
  </BoxAnnotation>

<IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Один-к-нескольким и Несколько-к-одному (и несколько-к-нескольким)

Конечно, вам не обязательно использовать только одну <ItemLink id="import_bus" /> (МЭ шину импорта), <ItemLink id="export_bus" /> (МЭ шину экспорта) или <ItemLink id="storage_bus" /> (МЭ шину хранения).

<GameScene zoom="3" background="transparent">
<ImportStructure src="../assets/assemblies/many_to_many_pipe.snbt" />

<IsometricCamera yaw="185" pitch="30" />
</GameScene>

## Подача в несколько мест

Из всего этого мы можем вывести метод отправки ингредиентов из одной стороны <ItemLink id="pattern_provider" /> (МЭ поставщика шаблонов) в несколько
разных мест, например, в массив машин или несколько разных сторон одной машины.

Мы не хотим использовать схему шина импорта -> шина хранения или шина хранения -> шина экспорта, потому что <ItemLink id="pattern_provider" /> (МЭ поставщик шаблонов) никогда
фактически не содержит ингредиенты. Вместо этого поставщики *передают* ингредиенты в соседние инвентари, поэтому нам нужен
соседний инвентарь, который также может импортировать предметы.

Это похоже на... <ItemLink id="interface" /> (МЭ-интерфейс)!
Убедитесь, что поставщик шаблонов находится в направленном или плоском подрежиме и/или интерфейс находится в плоском подрежиме, чтобы они не образовали сетевое
соединение.

<GameScene zoom="6" background="transparent">
<ImportStructure src="../assets/assemblies/provider_interface_storage.snbt" />

<BoxAnnotation color="#dddddd" min="2.7 0 1" max="3 1 2">
        МЭ-интерфейс (должен быть плоским, не полным блоком)
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="1 0 0" max="1.3 1 4">
        Шины хранения
  </BoxAnnotation>

<BoxAnnotation color="#dddddd" min="0 0 0" max="1 1 4">
        Места, куда вы хотите подавать шаблоны (несколько машин или несколько сторон одной машины)
  </BoxAnnotation>

<IsometricCamera yaw="185" pitch="30" />
</GameScene>