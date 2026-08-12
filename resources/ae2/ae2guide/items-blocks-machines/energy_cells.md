---
navigation:
  parent: items-blocks-machines-index.md
  title: МЭ ячейки энергии
  icon: energy_cell
  position: 110
categories:
- network infrastructure
item_ids:
- ae2:energy_cell
- ae2:dense_energy_cell
- ae2:creative_energy_cell
---

# МЭ ячейки энергии

<Row gap="3">
  <BlockImage id="energy_cell" scale="4" p:fullness="4" />
  <BlockImage id="dense_energy_cell" scale="4" p:fullness="4" />
  <BlockImage id="creative_energy_cell" scale="4" />
</Row>

МЭ ячейки энергии обеспечивают сети дополнительное хранилище [энергии](../ae2-mechanics/energy.md). Некоторый буфер энергии помогает сглаживать скачки энергопотребления при вставке или извлечении большого количества предметов, а большее хранилище энергии позволяет сети работать, когда энергия не генерируется (например, ночью с солнечными панелями) или справляться с огромным мгновенным энергопотреблением [пространственного хранилища](../ae2-mechanics/spatial-io.md).

## Индикаторы заполнения

<Row>
<BlockImage id="energy_cell" scale="4" p:fullness="0" />
<BlockImage id="energy_cell" scale="4" p:fullness="1" />
<BlockImage id="energy_cell" scale="4" p:fullness="2" />
<BlockImage id="energy_cell" scale="4" p:fullness="3" />
<BlockImage id="energy_cell" scale="4" p:fullness="4" />
</Row>

Полосы на стороне ячейки показывают уровень её заряда:

* 0 при заряде ниже 25%
* 1 при заряде от 25% до 50%
* 2 при заряде от 50% до 75%
* 3 при заряде от 75% до 99%
* 4 при заряде выше 99%

## Типы ячеек

* <ItemLink id="energy_cell" /> может хранить 200k AE и обычно достаточна для большинства случаев, легко справляясь с энергетическими скачками при нормальном использовании сети.
* <ItemLink id="dense_energy_cell" /> может хранить 1.6M AE и предназначена для работы сети от накопленной энергии или для обработки огромного мгновенного энергопотребления больших установок [пространственного хранилища](../ae2-mechanics/spatial-io.md).
* <ItemLink id="creative_energy_cell" /> — это креативный предмет для тестирования, предоставляющий НЕОГРАНИЧЕННУЮ ЭНЕРГИЮ.

## Рецепты

<Row>
  <RecipeFor id="energy_cell" />
  <RecipeFor id="dense_energy_cell" />
</Row>