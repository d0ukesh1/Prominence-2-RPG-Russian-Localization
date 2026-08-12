---
navigation:
    parent: epp_intro/epp_intro-index.md
    title: МЭ Точная шина экспорта
    icon: extendedae:precise_export_bus
categories:
- extended devices
item_ids:
- extendedae:precise_export_bus
---

# МЭ Точная шина экспорта

<GameScene zoom="8" background="transparent">
  <ImportStructure src="../structure/cable_precise_export_bus.snbt"></ImportStructure>
</GameScene>

МЭ Точная шина экспорта экспортирует предметы или жидкости в заданных количествах. Она экспортирует только в том случае, если контейнер может полностью принять весь объём вывода.

## Пример

![GUI](../pic/pre_bus_gui1.png)

Это означает экспорт 3 булыжников за операцию. Экспорт прекращается, если количество булыжников в сети меньше 3.

![GUI](../pic/pre_bus_gui2.png)

Экспорт также прекращается, если целевой контейнер не может вместить весь экспортируемый объём. Например, сундук может принять только 2 булыжника, поэтому шина экспорта останавливается.