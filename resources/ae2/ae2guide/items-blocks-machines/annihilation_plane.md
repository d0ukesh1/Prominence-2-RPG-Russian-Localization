---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: МЭ плоскость уничтожения
  icon: annihilation_plane
  position: 210
categories:
- devices
item_ids:
- ae2:annihilation_plane
---

# МЭ плоскость уничтожения

<GameScene zoom="8" background="transparent">
<ImportStructure src="../assets/blocks/annihilation_plane.snbt" />
</GameScene>

МЭ плоскость уничтожения ломает блоки и подбирает предметы. Она работает аналогично <ItemLink id="import_bus" />, отправляя предметы в [сетевое хранилище](../ae2-mechanics/import-export-storage.md). Чтобы предметы были подобраны, они должны соприкоснуться с поверхностью плоскости, она не подбирает предметы в области.

МЭ плоскости уничтожения можно зачаровать любыми зачарованиями для кирок, так что да, вы можете наложить высокий уровень "Удачи" на несколько плоскостей и [автоматизировать обработку руды](../example-setups/ore-fortuner.md), если ваш модпак это позволяет. Кроме того, "Шёлковое касание" работает, как ожидается, "Эффективность" снижает энергозатраты на разрушение блока, а "Прочность" даёт шанс не использовать энергию.

Они являются [субкомпонентами кабеля](../ae2-mechanics/cable-subparts.md).

**НЕ ЗАБУДЬТЕ ВКЛЮЧИТЬ ПОДДЕЛЬНЫХ ИГРОКОВ В ВАШЕМ ЧАНКЕ**

## Фильтрация

МЭ плоскость уничтожения будет ломать блок или подбирать предмет только если она может сохранить полученные предметы/дроп в своей сети. Это означает, что для фильтрации необходимо *ограничить, что может храниться в её сети*, скорее всего, поместив её в [подсеть](../ae2-mechanics/subnetworks.md). <ItemLink id="storage_bus" /> или [ячейку](../items-blocks-machines/storage_cells.md) можно [разделить](cell_workbench.md) для достижения этой цели.

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/annihilation_filtering.snbt" />

  <DiamondAnnotation pos="1 0.5 0.5" color="#00ff00">
        Отфильтровано по тому, что выпадает из блока, который вы хотите сломать.
  </DiamondAnnotation>

  <DiamondAnnotation pos=".5 0.5 2.5" color="#00ff00">
        Разделено по тому, что выпадает из блока, который вы хотите сломать.
  </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Ещё раз, фильтрация происходит *по выпадающим предметам*, так что, например, если вы хотите фильтровать разрушение <ItemLink id="minecraft:amethyst_cluster" />, вам нужна плоскость с зачарованием "Шёлковое касание", иначе каждая предыдущая стадия роста ничего не даёт, и плоскость будет ломать их независимо от настроек, так как сеть всегда может хранить "ничего".

## Рецепт

<RecipeFor id="annihilation_plane" />