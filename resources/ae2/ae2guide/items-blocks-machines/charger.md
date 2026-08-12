---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: МЭ зарядное устройство
  icon: charger
  position: 310
categories:
- machines
item_ids:
- ae2:charger
---

# МЭ зарядное устройство

<BlockImage id="charger" scale="8" />

МЭ зарядное устройство позволяет заряжать поддерживаемые инструменты и <ItemLink id="certus_quartz_crystal" />.

Энергия может подаваться сверху или снизу через [кабели](cables.md) AE2 или кабели энергии других модов. Оно может принимать как энергию AE2 (AE), так и энергию Forge (FE). Предметы можно вставлять или извлекать с любой стороны. Извлекать можно только результаты, так что нет необходимости в фильтрах, чтобы предотвратить извлечение кристаллов истинного кварца вместо заряженных. Можно повернуть с помощью <ItemLink id="certus_quartz_wrench" /> для удобства автоматизации.

Используется для создания <ItemLink id="charged_certus_quartz_crystal" /> из <ItemLink id="certus_quartz_crystal" /> и <ItemLink id="meteorite_compass" /> из <ItemLink id="minecraft:compass" />.

Для ручного питания установите <ItemLink id="crank" /> сверху или снизу и щёлкайте ПКМ, пока предмет не зарядится.

Также служит рабочей станцией для жителя AE2.

## Простая автоматизация

Например, возможность поворота позволяет полуавтоматизировать зарядные устройства следующим образом:

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/charger_hopper.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Рецепт

<RecipeFor id="charger" />