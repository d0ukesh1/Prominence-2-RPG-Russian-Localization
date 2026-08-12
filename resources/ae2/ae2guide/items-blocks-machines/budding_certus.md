---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: Цветущий истинный кварц
  icon: flawless_budding_quartz
  position: 010
categories:
- misc ingredients blocks
item_ids:
- ae2:flawless_budding_quartz
- ae2:flawed_budding_quartz
- ae2:chipped_budding_quartz
- ae2:damaged_budding_quartz
- ae2:small_quartz_bud
- ae2:medium_quartz_bud
- ae2:large_quartz_bud
- ae2:quartz_cluster
---

# Цветущий истинный кварц

(также см. [Выращивание истинного кварца](../ae2-mechanics/certus-growth.md))

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/budding_blocks.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Бутоны истинного кварца вырастают на цветущих блоках истинного кварца, подобно аметисту. Эти блоки можно найти в [метеоритах](../ae2-mechanics/meteorites.md). Существует 4 уровня цветущих блоков истинного кварца: безупречный, потрескавшийся, треснувший и повреждённый. Их легче всего идентифицировать с помощью модов, таких как HWYLA, Jade, The One Probe и т.д. (или с помощью экрана F3).

Для потрескавшихся, треснувших и повреждённых цветущих блоков истинного кварца каждый раз, когда бутон вырастает на следующую стадию, блок может понизиться на один уровень, в конечном итоге превращаясь в обычный <ItemLink id="quartz_block" />.

Безупречный цветущий истинный кварц не портится при росте бутонов и служит бесконечным источником.

Если сломать цветущий блок обычной киркой, он понизится на один уровень. Если использовать кирку с зачарованием "Шёлковое касание", блок не понизится, за исключением безупречного. **Это означает, что безупречные цветущие блоки истинного кварца нельзя поднять и перенести с помощью кирки**. Вместо этого можно использовать [Пространственное хранилище](../ae2-mechanics/spatial-io.md) для перемещения безупречных цветущих блоков.

## Рецепты

Потрескавшиеся, треснувшие и повреждённые цветущие блоки истинного кварца можно создать, поместив блок предыдущего уровня (или <ItemLink id="quartz_block" />) в воду с одним или несколькими <ItemLink id="charged_certus_quartz_crystal" />.

Безупречный цветущий истинный кварц нельзя создать, его можно только найти в мире.

<Row>
  <RecipeFor id="damaged_budding_quartz" />
  <RecipeFor id="chipped_budding_quartz" />
  <RecipeFor id="flawed_budding_quartz" />
</Row>