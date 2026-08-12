---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: Камеры хранения
  icon: item_storage_cell_1k
  position: 410
categories:
- tools
item_ids:
- ae2:item_cell_housing
- ae2:fluid_cell_housing
- ae2:cell_component_1k
- ae2:cell_component_4k
- ae2:cell_component_16k
- ae2:cell_component_64k
- ae2:cell_component_256k
- ae2:item_storage_cell_1k
- ae2:item_storage_cell_4k
- ae2:item_storage_cell_16k
- ae2:item_storage_cell_64k
- ae2:item_storage_cell_256k
- ae2:fluid_storage_cell_1k
- ae2:fluid_storage_cell_4k
- ae2:fluid_storage_cell_16k
- ae2:fluid_storage_cell_64k
- ae2:fluid_storage_cell_256k
---

# Камеры хранения

<Column>
  <Row>
    <ItemImage id="item_storage_cell_1k" scale="4" />
    <ItemImage id="item_storage_cell_4k" scale="4" />
    <ItemImage id="item_storage_cell_16k" scale="4" />
    <ItemImage id="item_storage_cell_64k" scale="4" />
    <ItemImage id="item_storage_cell_256k" scale="4" />
  </Row>

  <Row>
    <ItemImage id="fluid_storage_cell_1k" scale="4" />
    <ItemImage id="fluid_storage_cell_4k" scale="4" />
    <ItemImage id="fluid_storage_cell_16k" scale="4" />
    <ItemImage id="fluid_storage_cell_64k" scale="4" />
    <ItemImage id="fluid_storage_cell_256k" scale="4" />
  </Row>
</Column>

Камеры хранения — один из основных способов хранения в Applied Energistics 2. Они используются в <ItemLink id="drive" /> (МЭ-дисковод) или <ItemLink id="chest" /> (МЭ-сундук).

Подробное объяснение их ёмкости в байтах и типах см. в разделе [Байты и типы](../ae2-mechanics/bytes-and-types.md).

Компоненты хранения можно извлечь из корпуса, если камера пуста, с помощью Shift+ПКМ, держа камеру в руке.

## Ёмкость хранения при различном количестве типов

Из-за [предварительной стоимости типов](../ae2-mechanics/bytes-and-types.md) камера, содержащая 1 тип предметов, может хранить в 2 раза больше, чем камера с 63 типами.

| Камера                                   | Общая ёмкость при 1 типе | Общая ёмкость при 63 типах |
|------------------------------------------|--------------------------|----------------------------|
| <ItemLink id="item_storage_cell_1k" />   |                    8,128 |                      4,160 |
| <ItemLink id="item_storage_cell_4k" />   |                   32,512 |                     16,640 |
| <ItemLink id="item_storage_cell_16k" />  |                  130,048 |                     66,560 |
| <ItemLink id="item_storage_cell_64k" />  |                  520,192 |                    266,240 |
| <ItemLink id="item_storage_cell_256k" /> |                2,080,768 |                  1,064,960 |

## Разделение

Камеры можно настроить для принятия только определённых предметов, аналогично фильтрации <ItemLink id="storage_bus" /> (МЭ шина хранения). Это делается в <ItemLink id="cell_workbench" /> (Верстак для камер).

Предметы можно перетаскивать в слоты из JEI/REI, даже если у вас нет этих предметов.

## Улучшения

Камеры хранения поддерживают следующие [улучшения](upgrade_cards.md), которые устанавливаются через <ItemLink id="cell_workbench" /> (Верстак для камер):

* <ItemLink id="fuzzy_card" /> (Карта размытости, недоступна для жидкостных камер) позволяет разделять камеру по уровню повреждений и/или игнорировать NBT предметов.
* <ItemLink id="inverter_card" /> (Карта-инвертер) переключает фильтр с белого списка на чёрный.
* <ItemLink id="equal_distribution_card" /> (Карта равномерного распределения) выделяет одинаковое количество байтов для каждого типа, чтобы один тип не занимал всю камеру.
* <ItemLink id="void_card" /> (Пустотная карта) уничтожает предметы, если камера заполнена (или выделенное место для типа заполнено при использовании карты равномерного распределения). Полезно для предотвращения переполнения ферм. Обязательно настройте разделение!
* Переносные камеры могут принимать <ItemLink id="energy_card" /> (Энергетическая карта) для увеличения ёмкости батареи.

## Окрашивание

Переносные предметные и жидкостные камеры можно окрашивать, как кожаную броню, путём крафта с красителями.

# Корпуса

Камеры создаются из компонента хранения и корпуса или с использованием рецепта корпуса вокруг компонента хранения:

<Row>
  <Recipe id="network/cells/item_storage_cell_1k" />
  <Recipe id="network/cells/item_storage_cell_1k_storage" />
</Row>

Корпуса сами по себе создаются следующим образом:

<Row>
  <RecipeFor id="item_cell_housing" />
  <RecipeFor id="fluid_cell_housing" />
</Row>

# Компоненты хранения

Компоненты хранения — основа всех камер AE2, определяющая их ёмкость. Каждый уровень увеличивает ёмкость в 4 раза и требует 3 компонента предыдущего уровня.

<Column>
  <Row>
    <RecipeFor id="cell_component_1k" />
    <RecipeFor id="cell_component_4k" />
    <RecipeFor id="cell_component_16k" />
  </Row>

  <Row>
    <RecipeFor id="cell_component_64k" />
    <RecipeFor id="cell_component_256k" />
  </Row>
</Column>

# Предметные камеры хранения

Предметные камеры хранения могут содержать до 63 различных типов предметов и доступны во всех стандартных ёмкостях.

<Column>
  <Row>
    <Recipe id="network/cells/item_storage_cell_1k_storage" />
    <Recipe id="network/cells/item_storage_cell_4k_storage" />
    <Recipe id="network/cells/item_storage_cell_16k_storage" />
  </Row>

  <Row>
    <Recipe id="network/cells/item_storage_cell_64k_storage" />
    <Recipe id="network/cells/item_storage_cell_256k_storage" />
  </Row>
</Column>

## Переносное предметное хранение

Переносные камеры работают как небольшой <ItemLink id="chest" /> (МЭ-сундук) в вашем кармане или как рюкзак. Их можно заряжать в <ItemLink id="charger" /> (Зарядник).

В отличие от стандартных камер хранения, их ёмкость по типам *уменьшается* с увеличением байтовой ёмкости, а общая байтовая ёмкость составляет половину от стандартной.

Помимо улучшений, доступных всем камерам, эти камеры также принимают <ItemLink id="energy_card" /> (Энергетическая карта) для улучшения встроенных батарей.

<Column>
  <Row>
    <RecipeFor id="portable_item_cell_1k" />
    <RecipeFor id="portable_item_cell_4k" />
    <RecipeFor id="portable_item_cell_16k" />
  </Row>

  <Row>
    <RecipeFor id="portable_item_cell_64k" />
    <RecipeFor id="portable_item_cell_256k" />
  </Row>
</Column>

# Жидкостные камеры хранения

Жидкостные камеры хранения могут содержать до 5 различных типов жидкостей и доступны во всех стандартных ёмкостях.

<Column>
  <Row>
    <Recipe id="network/cells/fluid_storage_cell_1k_storage" />
    <Recipe id="network/cells/fluid_storage_cell_4k_storage" />
    <Recipe id="network/cells/fluid_storage_cell_16k_storage" />
  </Row>

  <Row>
    <Recipe id="network/cells/fluid_storage_cell_64k_storage" />
    <Recipe id="network/cells/fluid_storage_cell_256k_storage" />
  </Row>
</Column>

## Переносное жидкостное хранение

Переносные жидкостные камеры работают как небольшой <ItemLink id="chest" /> (МЭ-сундук) в вашем кармане или как рюкзак. Их можно заряжать в <ItemLink id="charger" /> (Зарядник).

В отличие от стандартных камер хранения, их ёмкость по типам *уменьшается* с увеличением байтовой ёмкости, а общая байтовая ёмкость составляет половину от стандартной.

Помимо улучшений, доступных всем камерам, эти камеры также принимают <ItemLink id="energy_card" /> (Энергетическая карта) для улучшения встроенных батарей.

<Column>
  <Row>
    <RecipeFor id="portable_fluid_cell_1k" />
    <RecipeFor id="portable_fluid_cell_4k" />
    <RecipeFor id="portable_fluid_cell_16k" />
  </Row>

  <Row>
    <RecipeFor id="portable_fluid_cell_64k" />
    <RecipeFor id="portable_fluid_cell_256k" />
  </Row>
</Column>

# Творческие предметные и жидкостные камеры

<Row>
  <ItemImage id="creative_item_cell" scale="2" />
  <ItemImage id="creative_fluid_cell" scale="2" />
</Row>

Творческие предметные и жидкостные камеры **не обеспечивают бесконечное хранение**. Вместо этого они выступают как бесконечные источники и поглотители предметов или жидкостей, для которых они [разделены](cell_workbench.md) (настроены в верстаке для камер).