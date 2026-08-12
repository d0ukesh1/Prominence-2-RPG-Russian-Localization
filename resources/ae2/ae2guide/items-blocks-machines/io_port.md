---
navigation:
  parent: items-blocks-machines-index.md
  title: МЭ порт ввода-вывода
  icon: io_port
  position: 210
categories:
- devices
item_ids:
- ae2:io_port
---

# МЭ порт ввода-вывода

<BlockImage id="io_port" p:powered="true" scale="8" />

МЭ порт ввода-вывода позволяет быстро заполнять или опустошать [МЭ камеры хранения](../items-blocks-machines/storage_cells.md) из или в [сетевое хранилище](../ae2-mechanics/import-export-storage.md).

Его можно поворачивать с помощью <ItemLink id="certus_quartz_wrench" />.

## Настройки

* МЭ порт ввода-вывода можно настроить на перемещение ячейки в выходные слоты, когда ячейка пуста, полна или когда работа завершена.
* Если установлена <ItemLink id="redstone_card" />, появятся опции для различных условий редстоуна.
* В центре интерфейса есть стрелка для установки направления передачи предметов: из ячейки в [сетевое хранилище](../ae2-mechanics/import-export-storage.md) или из хранилища в ячейку.

## Улучшения

МЭ порт ввода-вывода поддерживает следующие [улучшения](upgrade_cards.md):

* <ItemLink id="speed_card" /> увеличивает количество предметов, перемещаемых за операцию.
* <ItemLink id="redstone_card" /> добавляет управление редстоуном, позволяя активировать при высоком сигнале, низком сигнале или один раз за импульс.

## Рецепт

<RecipeFor id="io_port" />