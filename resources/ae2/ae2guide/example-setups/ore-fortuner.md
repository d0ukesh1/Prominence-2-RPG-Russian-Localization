---
navigation:
  parent: example-setups/example-setups-index.md
  title: Автоматизация добычи руды с удачей
  icon: minecraft:raw_iron
---

# Автоматизация добычи руды с удачей

<ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) можно зачаровать любым зачарованием для кирки, включая «Удачу», поэтому очевидное применение — зачаровать несколько плоскостей на удачу и использовать <ItemLink id="formation_plane" /> (МЭ плоскость формирования) и <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) для быстрого размещения и разрушения руд.

Обратите внимание, что поскольку <ItemLink id="import_bus" /> (МЭ шина импорта) «набирает скорость», установка начнёт работать медленно, но через несколько секунд достигнет полной скорости.

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/ore_fortuner.snbt" />

  <BoxAnnotation color="#dddddd" min="2.7 0 2" max="3 1 3">
        (1) МЭ шина импорта: Содержит несколько Карт ускорения.
        <ItemImage id="speed_card" scale="2" />
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="0 0 2" max="2 1 2.3">
        (2) МЭ плоскости формирования: В стандартной конфигурации.
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="0 0 0.7" max="2 1 1">
        (3) МЭ плоскости уничтожения: Без интерфейса для настройки, но зачарованы на «Удачу».
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="2.7 0 0" max="3 1 1">
        (4) МЭ шина хранения: В стандартной конфигурации.
  </BoxAnnotation>

<DiamondAnnotation pos="3.5 0.5 2.5" color="#00ff00">
        Вход
    </DiamondAnnotation>

<DiamondAnnotation pos="3.5 0.5 0.5" color="#00ff00">
        Выход
    </DiamondAnnotation>

<DiamondAnnotation pos="4 0.5 1.5" color="#00ff00">
        К основной сети
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Настройки

* <ItemLink id="import_bus" /> (МЭ шина импорта) (1) содержит несколько <ItemLink id="speed_card" /> (Карт ускорения). Чем больше плоскостей формирования в массиве, тем больше карт требуется, так как они позволяют шине импорта извлекать больше предметов одновременно.
* <ItemLink id="formation_plane" /> (МЭ плоскости формирования) (2) находятся в стандартной конфигурации.
* <ItemLink id="annihilation_plane" /> (МЭ плоскости уничтожения) (3) не имеют интерфейса и не могут быть настроены, но зачарованы на «Удачу».
* <ItemLink id="storage_bus" /> (МЭ шина хранения) (4) находится в стандартной конфигурации.

## Как это работает

1. <ItemLink id="import_bus" /> (МЭ шина импорта) на зелёной подсети импортирует блоки из первой бочки в [сетевое хранилище](../ae2-mechanics/import-export-storage.md).
2. Единственное хранилище в зелёной подсети — <ItemLink id="formation_plane" /> (МЭ плоскость формирования), которая размещает блоки.
3. <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) на оранжевой подсети разрушает блоки, применяя к ним эффект «Удачи».
4. <ItemLink id="storage_bus" /> (МЭ шина хранения) на оранжевой подсети сохраняет результаты разрушения во вторую бочку.