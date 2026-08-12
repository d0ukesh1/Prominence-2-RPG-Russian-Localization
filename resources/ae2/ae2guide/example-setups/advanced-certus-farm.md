---
navigation:
  parent: example-setups/example-setups-index.md
  title: Продвинутая ферма истинного кварца
  icon: certus_quartz_crystal
  position: 120
---

# Продвинутая ферма истинного кварца

Это, по сути, [полуавтоматическая ферма истинного кварца](semiauto-certus-farm.md), но полностью интегрированная в вашу МЭ-систему.

Вместо того чтобы иметь большой запас цветущих блоков и вручную обновлять их время от времени, эта установка использует [автоматизацию зарядника](charger-automation.md) и [автоматизацию погружения в воду](throw-in-water-automation.md) для выполнения этого процесса автоматически.

**ЭТО СЛОЖНАЯ КОНСТРУКЦИЯ С ЭЛЕМЕНТАМИ, СКРЫТЫМИ ЗА ДРУГИМИ. ПОВОРАЧИВАЙТЕ КАМЕРУ, ЧТОБЫ РАССМОТРЕТЬ ЕЁ СО ВСЕХ СТОРОН**

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/advanced_certus_farm.snbt" />

  <BoxAnnotation color="#ddaaaa" min="3.7 2 1" max="4 3 2">
        (1) МЭ плоскость уничтожения №1: Без интерфейса для настройки, но может быть зачарована на «Удачу».
  </BoxAnnotation>

  <BoxAnnotation color="#ddaaaa" min="2 2 1.7" max="3 3 2">
        (2) МЭ шина хранения №1: Отфильтрована на Кристалл истинного кварца.
        <ItemImage id="certus_quartz_crystal" scale="2" />
  </BoxAnnotation>

  <DiamondAnnotation pos="3 2.5 1.5" color="#ff0000">
    Подсеть разрушения друзы
  </DiamondAnnotation>

  <BoxAnnotation color="#aaddaa" min="3.7 1 1" max="4 2 2">
        (3) МЭ плоскость уничтожения №2: Без интерфейса для настройки, но зачарована на «Шёлковое касание».
  </BoxAnnotation>

  <BoxAnnotation color="#aaddaa" min="2 1 1.7" max="3 2 2">
        (4) МЭ шина хранения №2: Отфильтрована на Блок истинного кварца.
        <BlockImage id="quartz_block" scale="2" />
  </BoxAnnotation>

  <DiamondAnnotation pos="3 1.5 1.5" color="#00ff00">
    Подсеть разрушения блока истинного кварца
  </DiamondAnnotation>

  <BoxAnnotation color="#ffddaa" min="4 0.7 1" max="5 1 2">
        (5) МЭ плоскость формирования: В стандартной конфигурации.
  </BoxAnnotation>

  <BoxAnnotation color="#ffddaa" min="2 0.7 2" max="3 1 3">
        (6) МЭ шина импорта: Отфильтрована на Потресканный цветущий блок истинного кварца.
        <BlockImage id="flawed_budding_quartz" scale="2" />
  </BoxAnnotation>

  <DiamondAnnotation pos="3 0.5 1.5" color="#ddcc00">
    Подсеть размещения цветущего блока
  </DiamondAnnotation>

  <BoxAnnotation color="#aaaadd" min="1.7 2 2" max="2 3 3">
        (7) МЭ шина хранения №3: Отфильтрована на Кристалл истинного кварца. Имеет приоритет выше, чем у основного хранилища.
        <ItemImage id="certus_quartz_crystal" scale="2" />
  </BoxAnnotation>

  <BoxAnnotation color="#aaaadd" min="2 1 2" max="3 2 3">
        (8) МЭ-интерфейс: Настроен на хранение 1 Потресканного цветущего блока истинного кварца, содержит Карту изготовления.
        <Row><BlockImage id="flawed_budding_quartz" scale="2" /> <ItemImage id="crafting_card" scale="2" /></Row>
  </BoxAnnotation>

<DiamondAnnotation pos="1.5 0.5 0" color="#00ff00">
        К основной сети, автоматизации зарядника и автоматизации погружения в воду
        <Row>
        <GameScene zoom="3" background="transparent">
          <ImportStructure src="../assets/assemblies/charger_automation.snbt" />
          <IsometricCamera yaw="195" pitch="30" />
        </GameScene>
        <GameScene zoom="3" background="transparent">
          <ImportStructure src="../assets/assemblies/throw_in_water.snbt" />
          <IsometricCamera yaw="195" pitch="30" />
        </GameScene>
        </Row>
    </DiamondAnnotation>

  <IsometricCamera yaw="165" pitch="5" />
</GameScene>

## Настройки

### Подсеть разрушения друзы:

* Первая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) (1) не имеет интерфейса и не может быть настроена, но может быть зачарована на «Удачу».
* Первая <ItemLink id="storage_bus" /> (МЭ шина хранения) (2) отфильтрована на <ItemLink id="certus_quartz_crystal" /> (Кристалл истинного кварца).

### Подсеть разрушения блока истинного кварца:

* Вторая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) (3) не имеет интерфейса и не может быть настроена, но должна быть зачарована на «Шёлковое касание».
* Вторая <ItemLink id="storage_bus" /> (МЭ шина хранения) (4) отфильтрована на <ItemLink id="quartz_block" /> (Блок истинного кварца).

### Подсеть размещения цветущего блока:

* <ItemLink id="formation_plane" /> (МЭ плоскость формирования) (5) находится в стандартной конфигурации.
* <ItemLink id="import_bus" /> (МЭ шина импорта) (6) отфильтрована на <ItemLink id="flawed_budding_quartz" /> (Потресканный цветущий блок истинного кварца).

### На основной сети:

* Третья <ItemLink id="storage_bus" /> (МЭ шина хранения) (7) отфильтрована на <ItemLink id="certus_quartz_crystal" /> (Кристалл истинного кварца) и имеет [приоритет](../ae2-mechanics/import-export-storage.md#storage-priority) выше, чем у основного хранилища.
* <ItemLink id="interface" /> (МЭ-интерфейс) (8) настроен на хранение 1 <ItemLink id="flawed_budding_quartz" /> (Потресканного цветущего блока истинного кварца) и содержит <ItemLink id="crafting_card" /> (Карту изготовления).

## Как это работает

### Подсеть разрушения друзы:

Подсеть разрушения друзы работает аналогично подсети в [простой ферме истинного кварца](simple-certus-farm.md).

1. <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) пытается разрушить то, что находится перед ней, но может разрушить только <ItemLink id="quartz_cluster" /> (Друзу истинного кварца), так как единственное хранилище в подсети — <ItemLink id="storage_bus" /> (МЭ шина хранения), отфильтрованная на <ItemLink id="certus_quartz_crystal" /> (Кристалл истинного кварца).
2. <ItemLink id="storage_bus" /> (МЭ шина хранения) сохраняет кристаллы истинного кварца в бочку.

### Подсеть разрушения блока истинного кварца

Подсеть разрушения блока истинного кварца служит для разрушения истощённого цветущего блока, когда он превращается в обычный <ItemLink id="quartz_block" /> (Блок истинного кварца). Она работает аналогично подсети разрушения друзы.

1. <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) пытается разрушить то, что находится перед ней, но может разрушить только <ItemLink id="quartz_block" /> (Блок истинного кварца), так как единственное хранилище в подсети — <ItemLink id="storage_bus" /> (МЭ шина хранения), отфильтрованная на <ItemLink id="quartz_block" /> (Блок истинного кварца). Плоскость должна быть зачарована на «Шёлковое касание», чтобы цветущий блок не портился при разрушении, и, таким образом, плоскость не разрушит его преждевременно.
2. <ItemLink id="storage_bus" /> (МЭ шина хранения) сохраняет блок истинного кварца в <ItemLink id="interface" /> (МЭ-интерфейс), позволяя [автоматизации погружения в воду](throw-in-water-automation.md) использовать его для создания нового <ItemLink id="flawed_budding_quartz" /> (Потресканного цветущего блока истинного кварца).

### Подсеть размещения цветущего блока

Подсеть размещения цветущего блока служит для размещения нового <ItemLink id="flawed_budding_quartz" /> (Потресканного цветущего блока истинного кварца), когда подсеть разрушения блока разрушает старый истощённый блок.

1. <ItemLink id="import_bus" /> (МЭ шина импорта) импортирует цветущий блок из <ItemLink id="interface" /> (МЭ-интерфейса) в [сетевое хранилище](../ae2-mechanics/import-export-storage.md).
2. Единственное хранилище в подсети — <ItemLink id="formation_plane" /> (МЭ плоскость формирования), которая размещает цветущий блок.

### На основной сети

* <ItemLink id="storage_bus" /> (МЭ шина хранения) предоставляет основной сети (а также [автоматизации зарядника](charger-automation.md)) доступ ко всем кристаллам истинного кварца в бочке. Она настроена на высокий [приоритет](../ae2-mechanics/import-export-storage.md#storage-priority), чтобы кристаллы истинного кварца предпочтительно возвращались в бочку, а не в основное хранилище.
* <ItemLink id="interface" /> (МЭ-интерфейс) предоставляет подсети размещения цветущего блока доступ к <ItemLink id="flawed_budding_quartz" /> (Потресканному цветущему блоку истинного кварца) и даёт подсети разрушения блока возможность возвращать истощённые блоки в основную сеть. <ItemLink id="crafting_card" /> (Карта изготовления) позволяет интерфейсу запрашивать новые цветущие блоки из системы [автоизготовления](../ae2-mechanics/autocrafting.md) основной сети.