---
navigation:
  parent: items-blocks-machines/items-blocks-machines-index.md
  title: МЭ процессор крафта (Хранилище, Сопроцессор, Монитор, Блок)
  icon: 1k_crafting_storage
  position: 210
categories:
- devices
item_ids:
- ae2:1k_crafting_storage
- ae2:4k_crafting_storage
- ae2:16k_crafting_storage
- ae2:64k_crafting_storage
- ae2:256k_crafting_storage
- ae2:crafting_accelerator
- ae2:crafting_monitor
- ae2:crafting_unit
---

# МЭ процессор крафта

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/crafting_cpus.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<Row>
  <BlockImage id="1k_crafting_storage" scale="4" />
  <BlockImage id="crafting_accelerator" scale="4" />
  <BlockImage id="crafting_monitor" scale="4" />
  <BlockImage id="crafting_unit" scale="4" />
</Row>

МЭ процессоры крафта управляют запросами/заданиями на крафт. Они хранят промежуточные ингредиенты во время выполнения заданий с несколькими шагами, влияют на размер заданий и, в некоторой степени, на скорость их выполнения. Подробнее см. в [автокрафте](../ae2-mechanics/autocrafting.md).

Каждый МЭ процессор крафта обрабатывает один запрос или задание, так что, если вы хотите одновременно запросить вычислительный процессор и 256 гладкого камня, вам нужно 2 многоблочные процессора.

Их можно настроить для обработки запросов от игроков, автоматизации (МЭ шины экспорта и МЭ-интерфейсы) или и того, и другого.

ПКМ по процессору открывает интерфейс статуса крафта, где можно проверить прогресс выполняемого задания.

## Настройки

* Процессор можно настроить на приём запросов только от игроков, только от автоматизации (например, <ItemLink id="export_bus" /> с <ItemLink id="crafting_card" />) или от обоих.

## Конструкция

МЭ процессоры крафта — это многоблочные структуры, которые должны быть сплошными прямоугольными призмами без зазоров. Они состоят из нескольких компонентов.

Каждый процессор должен содержать хотя бы один блок хранилища крафта (минимально жизнеспособный процессор — это один блок МЭ хранилища крафта 1k).

# МЭ блок крафта

<BlockImage id="crafting_unit" scale="4" />

(Опционально) МЭ блоки крафта просто заполняют пространство в процессоре, чтобы сделать его сплошной прямоугольной призмой, если у вас недостаточно других компонентов. Также являются базовым ингредиентом для других компонентов.

<RecipeFor id="crafting_unit" />

# МЭ хранилище крафта

<Row>
  <BlockImage id="1k_crafting_storage" scale="4" />
  <BlockImage id="4k_crafting_storage" scale="4" />
  <BlockImage id="16k_crafting_storage" scale="4" />
  <BlockImage id="64k_crafting_storage" scale="4" />
  <BlockImage id="256k_crafting_storage" scale="4" />
</Row>

(Обязательно) МЭ хранилища крафта доступны во всех стандартных размерах ячеек (1k, 4k, 16k, 64k, 256k). Они хранят ингредиенты и промежуточные ингредиенты, участвующие в крафте, поэтому для больших заданий с большим количеством ингредиентов требуется больше или крупнее хранилища.

<Column>
  <Row>
    <RecipeFor id="1k_crafting_storage" />
    <RecipeFor id="4k_crafting_storage" />
    <RecipeFor id="16k_crafting_storage" />
  </Row>
  <Row>
    <RecipeFor id="64k_crafting_storage" />
    <RecipeFor id="256k_crafting_storage" />
  </Row>
</Column>

# МЭ сопроцессор крафта

<BlockImage id="crafting_accelerator" scale="4" />

(Опционально) МЭ сопроцессоры крафта заставляют систему чаще отправлять партии ингредиентов из <ItemLink id="pattern_provider" />. Это позволяет им справляться с машинами, которые обрабатывают быстро. Например, МЭ поставщик шаблонов, окружённый <ItemLink id="molecular_assembler" />, может отправлять ингредиенты быстрее, чем один сборщик может обработать, распределяя партии между окружающими сборщиками.

<RecipeFor id="crafting_accelerator" />

# МЭ монитор крафта

<BlockImage id="crafting_monitor" scale="4" />

(Опционально) МЭ монитор крафта отображает задание, которое процессор выполняет в данный момент. Экран можно окрасить с помощью <ItemLink id="color_applicator" />.

<RecipeFor id="crafting_monitor" />