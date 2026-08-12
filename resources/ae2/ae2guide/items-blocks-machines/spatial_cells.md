---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: Пространственные камеры хранения
  icon: spatial_storage_cell_128
  position: 410
categories:
- tools
item_ids:
- ae2:spatial_storage_cell_2
- ae2:spatial_storage_cell_16
- ae2:spatial_storage_cell_128
- ae2:spatial_cell_component_2
- ae2:spatial_cell_component_16
- ae2:spatial_cell_component_128
---

# Пространственные камеры хранения

<Row>
  <ItemImage id="spatial_storage_cell_2" scale="4" />
  <ItemImage id="spatial_storage_cell_16" scale="4" />
  <ItemImage id="spatial_storage_cell_128" scale="4" />
</Row>

Пространственные камеры storage используются для [хранения физических объёмов пространства](../ae2-mechanics/spatial-io.md). 
Они применяются в <ItemLink id="spatial_io_port" /> (Пространственный порт ввода/вывода).

В отличие от [камер хранения](../items-blocks-machines/storage_cells.md), пространственные камеры нельзя переформатировать.

**Пространственную камеру НЕЛЬЗЯ СБРОСИТЬ, ПЕРЕФОРМАТИРОВАТЬ ИЛИ ИЗМЕНИТЬ РАЗМЕР ПОСЛЕ ИСПОЛЬЗОВАНИЯ.** Создайте новую камеру, если нужны другие размеры.

## Рецепты

<Row>
  <Recipe id="network/cells/spatial_storage_cell_2_cubed_storage" />
  <Recipe id="network/cells/spatial_storage_cell_16_cubed_storage" />
  <Recipe id="network/cells/spatial_storage_cell_128_cubed_storage" />
</Row>

# Корпуса

Камеры создаются из пространственного компонента и корпуса или с использованием рецепта корпуса вокруг пространственного компонента:

<Row>
  <Recipe id="network/cells/spatial_storage_cell_2_cubed" />
  <Recipe id="network/cells/spatial_storage_cell_2_cubed_storage" />
</Row>

Корпуса сами по себе создаются следующим образом:

<RecipeFor id="item_cell_housing" />

# Пространственные компоненты

Пространственные компоненты — основа пространственных камер хранения. Каждый уровень увеличивает размеры хранимого объёма в 8 раз.

<Row>
  <RecipeFor id="spatial_cell_component_2" />
  <RecipeFor id="spatial_cell_component_16" />
  <RecipeFor id="spatial_cell_component_128" />
</Row>