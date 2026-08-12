---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: Шина переключения
  icon: toggle_bus
  position: 110
categories:
- network infrastructure
item_ids:
- ae2:toggle_bus
- ae2:inverted_toggle_bus
---

# Шина переключения

<GameScene zoom="8" background="transparent">
<ImportStructure src="../assets/assemblies/toggle_bus.snbt" />
<IsometricCamera yaw="195" pitch="30" />
</GameScene>

Шина, которая функционирует аналогично <ItemLink id="fluix_glass_cable" /> (МЭ флюисовый стеклянный кабель) или другим кабелям, но позволяет переключать состояние соединения с помощью редстоуна. Это позволяет отключать часть [МЭ сети](../ae2-mechanics/me-network-connections.md).

При подаче сигнала редстоуна шина включает соединение, а <ItemLink id="inverted_toggle_bus" /> (МЭ перевёрнутая шина переключения) действует наоборот, отключая соединение.

Переключение может вызвать перезагрузку сети и пересчёт подключённых устройств.

Они являются [подчастями кабеля](../ae2-mechanics/cable-subparts.md).

## Рецепты

<RecipeFor id="toggle_bus" />
<RecipeFor id="inverted_toggle_bus" />