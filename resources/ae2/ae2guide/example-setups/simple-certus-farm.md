---
navigation:
  parent: example-setups/example-setups-index.md
  title: Простая ферма кварца цертуса
  icon: certus_quartz_crystal
  position: 110
---

# Простая ферма кварца цертуса

Как указано в [Росте кварца цертуса](../ae2-mechanics/certus-growth.md), автоматизация сбора <ItemLink id="certus_quartz_crystal" /> (Кристалл кварца цертуса) включает использование <ItemLink id="annihilation_plane" /> (Плоскостей уничтожения) и <ItemLink id="storage_bus" /> (Шин хранения). <ItemLink id="growth_accelerator" /> (Ускоритель роста) значительно ускоряет рост бутонов кварца цертуса, после чего плоскости уничтожения ломают полностью выросшие <ItemLink id="quartz_cluster" /> (Кластеры кварца). Фильтрация осуществляется благодаря удобной особенности: незрелые бутоны кварца при разрушении дают <ItemLink id="certus_quartz_dust" /> (Пыль кварца цертуса), а не ничего.

Эта ферма работает полностью автоматически с <ItemLink id="flawless_budding_quartz" /> (Безупречный растущий кварц), но с неполноценным, треснутым или повреждённым растущим кварцем цертуса вам придётся вручную заменять растущий блок. Или, как описано в [Полуавтоматическая ферма цертуса](semiauto-certus-farm.md) и [Продвинутая ферма цертуса](advanced-certus-farm.md), это можно автоматизировать.

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/simple_certus_farm.snbt" />

  <BoxAnnotation color="#dddddd" min="3.7 1 1" max="4 2 2">
        (1) Плоскость уничтожения: Без интерфейса настройки, но можно зачаровать на Удачу.
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="3 1 1" max="3.3 2 2">
        (2) Шина хранения №1: Отфильтрована на кристалл кварца цертуса.
        <ItemLink id="certus_quartz" />
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="3 1 .7" max="2 2 1">
        (3) Шина хранения №2: Отфильтрована на кристалл кварца цертуса. Приоритет выше, чем у основного хранилища.
        <ItemLink id="certus_quartz" />
  </BoxAnnotation>

<DiamondAnnotation pos="1 0.5 0.5" color="#00ff00">
        К основной сети
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Настройки

* Первая <ItemLink id="annihilation_plane" /> (Плоскость уничтожения) (1): Без интерфейса настройки, но можно зачаровать на Удачу.
* Первая <ItemLink id="storage_bus" /> (Шина хранения) (2): Отфильтрована на <ItemLink id="certus_quartz_crystal" /> (Кристалл кварца цертуса).
* Вторая <ItemLink id="storage_bus" /> (Шина хранения) (3): Отфильтрована на <ItemLink id="certus_quartz_crystal" /> (Кристалл кварца цертуса), с [приоритетом](../ae2-mechanics/import-export-storage.md#storage-priority) выше, чем у основного хранилища.

## Как это работает

1. <ItemLink id="annihilation_plane" /> (Плоскость уничтожения) пытается сломать то, что перед ней, но может сломать только <ItemLink id="quartz_cluster" /> (Кластер кварца), так как единственное хранилище на подсети — <ItemLink id="storage_bus" /> (Шина хранения), отфильтрованная на <ItemLink id="certus_quartz_crystal" /> (Кристалл кварца цертуса).
2. Первая <ItemLink id="storage_bus" /> (Шина хранения) сохраняет кристаллы кварца цертуса в бочку.
3. Вторая <ItemLink id="storage_bus" /> (Шина хранения) предоставляет основной сети доступ ко всем кристаллам кварца цертуса в бочке. Она настроена на высокий [приоритет](../ae2-mechanics/import-export-storage.md#storage-priority), чтобы кристаллы возвращались в бочку, а не в основное хранилище.