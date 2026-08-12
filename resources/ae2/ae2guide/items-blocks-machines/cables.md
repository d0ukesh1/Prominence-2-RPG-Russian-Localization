---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: МЭ кабели
  icon: fluix_glass_cable
  position: 110
categories:
- network infrastructure
item_ids:
- ae2:white_glass_cable
- ae2:orange_glass_cable
- ae2:magenta_glass_cable
- ae2:light_blue_glass_cable
- ae2:yellow_glass_cable
- ae2:lime_glass_cable
- ae2:pink_glass_cable
- ae2:gray_glass_cable
- ae2:light_gray_glass_cable
- ae2:cyan_glass_cable
- ae2:purple_glass_cable
- ae2:blue_glass_cable
- ae2:brown_glass_cable
- ae2:green_glass_cable
- ae2:red_glass_cable
- ae2:black_glass_cable
- ae2:fluix_glass_cable
- ae2:white_covered_cable
- ae2:orange_covered_cable
- ae2:magenta_covered_cable
- ae2:light_blue_covered_cable
- ae2:yellow_covered_cable
- ae2:lime_covered_cable
- ae2:pink_covered_cable
- ae2:gray_covered_cable
- ae2:light_gray_covered_cable
- ae2:cyan_covered_cable
- ae2:purple_covered_cable
- ae2:blue_covered_cable
- ae2:brown_covered_cable
- ae2:green_covered_cable
- ae2:red_covered_cable
- ae2:black_covered_cable
- ae2:fluix_covered_cable
- ae2:white_covered_dense_cable
- ae2:orange_covered_dense_cable
- ae2:magenta_covered_dense_cable
- ae2:light_blue_covered_dense_cable
- ae2:yellow_covered_dense_cable
- ae2:lime_covered_dense_cable
- ae2:pink_covered_dense_cable
- ae2:gray_covered_dense_cable
- ae2:light_gray_covered_dense_cable
- ae2:cyan_covered_dense_cable
- ae2:purple_covered_dense_cable
- ae2:blue_covered_dense_cable
- ae2:brown_covered_dense_cable
- ae2:green_covered_dense_cable
- ae2:red_covered_dense_cable
- ae2:black_covered_dense_cable
- ae2:fluix_covered_dense_cable
- ae2:white_smart_cable
- ae2:orange_smart_cable
- ae2:magenta_smart_cable
- ae2:light_blue_smart_cable
- ae2:yellow_smart_cable
- ae2:lime_smart_cable
- ae2:pink_smart_cable
- ae2:gray_smart_cable
- ae2:light_gray_smart_cable
- ae2:cyan_smart_cable
- ae2:purple_smart_cable
- ae2:blue_smart_cable
- ae2:brown_smart_cable
- ae2:green_smart_cable
- ae2:red_smart_cable
- ae2:black_smart_cable
- ae2:fluix_smart_cable
- ae2:white_smart_dense_cable
- ae2:orange_smart_dense_cable
- ae2:magenta_smart_dense_cable
- ae2:light_blue_smart_dense_cable
- ae2:yellow_smart_dense_cable
- ae2:lime_smart_dense_cable
- ae2:pink_smart_dense_cable
- ae2:gray_smart_dense_cable
- ae2:light_gray_smart_dense_cable
- ae2:cyan_smart_dense_cable
- ae2:purple_smart_dense_cable
- ae2:blue_smart_dense_cable
- ae2:brown_smart_dense_cable
- ae2:green_smart_dense_cable
- ae2:red_smart_dense_cable
- ae2:black_smart_dense_cable
- ae2:fluix_smart_dense_cable
---

# МЭ кабели

<GameScene zoom="3" background="transparent">
  <ImportStructure src="../assets/assemblies/cables.snbt" />
  <IsometricCamera yaw="180" pitch="30" />
</GameScene>

Хотя МЭ-сети также создаются соседними машинами с поддержкой МЭ, кабели — это основной способ расширения МЭ-сети на большие территории.

Кабели разных цветов можно использовать, чтобы соседние кабели не соединялись друг с другом, что позволяет более эффективно распределять [каналы](../ae2-mechanics/channels.md). Они также влияют на цвет терминалов, подключённых к ним, так что вам не придётся делать все терминалы фиолетовыми. Флюисовые кабели соединяются с кабелями любого другого цвета.

Обратите внимание, **КАНАЛЫ НЕ ИМЕЮТ НИЧЕГО ОБЩЕГО С ЦВЕТОМ КАБЕЛЯ**

## Важное замечание

**Если вы новичок в AE2 и не знакомы с каналами, используйте МЭ умные кабели и МЭ плотные умные кабели везде, где это возможно. Они показывают, как каналы направляются через вашу сеть, делая их поведение более понятным.**

## Ещё одно замечание

**Это не трубы для предметов, жидкостей, энергии и т.д.** У них нет внутреннего инвентаря, МЭ поставщики шаблонов и машины не "отправляют" в них ничего, всё, что они делают, — это соединяют [устройства](../ae2-mechanics/devices.md) AE2 в сеть.

## МЭ стеклянный кабель

<GameScene zoom="6" background="transparent">
<ImportStructure src="../assets/assemblies/fluix_glass_cable.snbt" />
<IsometricCamera yaw="195" pitch="30" />
</GameScene>

<ItemLink id="fluix_glass_cable" /> — самый простой в изготовлении кабель, передаёт энергию и до 8 [каналов](../ae2-mechanics/channels.md). Он доступен в 17 различных цветах, по умолчанию флюисовый, и может быть окрашен в любой цвет с использованием 16 красителей.

Для создания цветных кабелей окружите краситель любого типа 8 кабелями одного типа (цвет кабелей не имеет значения, но они должны быть одного типа: стеклянные, умные и т.д.). Вы также можете окрашивать кабели в мире с помощью любой кисти, совместимой с Forge.

Вы можете очистить цветной кабель с помощью ведра воды, чтобы удалить краситель.

Кабель можно покрыть шерстью, чтобы создать <ItemLink id="fluix_covered_cable" />, или изготовить <ItemLink id="fluix_smart_cable" />, чтобы лучше понимать, что происходит с вашими [каналами](../ae2-mechanics/channels.md).

<RecipeFor id="fluix_glass_cable" />

<RecipeFor id="blue_glass_cable" />

## МЭ покрытый кабель

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/fluix_covered_cable.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Вариант покрытого кабеля не имеет игровых преимуществ по сравнению с <ItemLink id="fluix_glass_cable" />. Однако он может использоваться как альтернативный эстетический выбор, если вам нравится покрытый вид.

Его можно окрасить так же, как <ItemLink id="fluix_glass_cable" />. Четыре <ItemLink id="fluix_covered_cable" /> можно скрафтить с редстоуном и светопылью, чтобы получить <ItemLink id="fluix_covered_dense_cable" />.

<Recipe id="network/cables/covered_fluix" />

<RecipeFor id="blue_covered_cable" />

## МЭ плотный кабеля

<GameScene zoom="6" >
  <ImportStructure src="../assets/assemblies/fluix_covered_cable.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Кабель повышенной пропускной способности, может передавать 32 канала, в отличие от стандартного кабеля, который поддерживает только 8. Однако он не поддерживает шины, поэтому сначала необходимо перейти на кабель меньшего размера (например, <ItemLink id="fluix_glass_cable" /> или <ItemLink id="fluix_smart_cable" />), прежде чем использовать шины или панели.

Плотные кабели слегка изменяют поведение "кратчайшего пути" каналов: каналы выбирают кратчайший путь к плотному кабелю, а затем кратчайший путь через этот плотный кабель к МЭ-регулятору.

<Recipe id="network/cables/dense_covered_fluix" />

<RecipeFor id="blue_covered_dense_cable" />

## МЭ умный кабель

<Row>
<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/fluix_smart_cable.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>
<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/fluix_smart_dense_cable.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>
</Row>

Хотя МЭ умные кабели внешне похожи на <ItemLink id="fluix_covered_cable" />, они выполняют диагностическую функцию, визуализируя использование каналов на кабелях. Каналы отображаются как светящиеся цветные линии, идущие вдоль чёрной полосы на кабелях, что даёт понимание того, как используются каналы в вашей сети. Для обычных умных кабелей первые четыре канала отображаются линиями, соответствующими цвету кабеля, следующие четыре — белыми линиями. Для плотных умных кабелей каждая полоса представляет 4 канала.

В сетях с <ItemLink id="controller" /> линии на кабелях показывают точный путь, по которому проходят каналы.

МЭ умные кабели во временных сетях показывают общее количество используемых каналов по всей сети, а не количество каналов, проходящих через конкретный кабель.

Их также можно окрасить так же, как <ItemLink id="fluix_glass_cable" />.

<Recipe id="network/cables/smart_fluix" />

<Recipe id="network/cables/dense_smart_fluix" />

<RecipeFor id="blue_smart_cable" />