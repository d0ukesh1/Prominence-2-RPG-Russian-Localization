---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: МЭ регулятор
  icon: controller
  position: 110
categories:
- network infrastructure
item_ids:
- ae2:controller
---

# МЭ регулятор

<BlockImage id="controller" p:state="online" scale="8" />

МЭ регулятор — это маршрутизационный центр [МЭ-сети](../ae2-mechanics/me-network-connections.md). Без него сеть является "временной" и может содержать не более 8 [устройств](../ae2-mechanics/devices.md), использующих каналы.

В одной [МЭ-сети](../ae2-mechanics/me-network-connections.md) не может быть двух регуляторов.

МЭ регулятор предоставляет 32 [канала](../ae2-mechanics/channels.md) на каждую сторону.

Для работы регулятору требуется 6 AE/т на каждый блок регулятора. Каждый блок регулятора может хранить 8000 AE, поэтому для больших сетей может потребоваться дополнительное хранилище энергии. Подробнее см. в [энергии](../ae2-mechanics/energy.md).

Многоблочные регуляторы могут быть построены в довольно свободной форме.

<GameScene zoom="2" background="transparent">
  <ImportStructure src="../assets/assemblies/controllers.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Однако необходимо соблюдать несколько правил:

1. Все блоки регулятора в [МЭ-сети](../ae2-mechanics/me-network-connections.md) должны быть соединены, иначе блоки станут красными.
2. Размер регулятора должен быть в пределах 7x7x7, иначе он станет красным.
3. У блока регулятора может быть не более 2 соседних блоков по одной оси; если это правило нарушено, блок отключится и станет красным.

<GameScene zoom="2" background="transparent">
  <ImportStructure src="../assets/assemblies/controller_rules.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Если все правила соблюдены и регулятор запитан, он должен светиться и менять цвета.

ПКМ по регулятору открывает тот же интерфейс, что и у <ItemLink id="network_tool" />.

## Рецепт

<RecipeFor id="controller" />