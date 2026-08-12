---
navigation:
  parent: items-blocks-machines-index.md
  title: Процессоры
  icon: logic_processor
  position: 010
categories:
- misc ingredients blocks
item_ids:
- ae2:logic_processor
- ae2:calculation_processor
- ae2:engineering_processor
- ae2:printed_silicon
- ae2:printed_logic_processor
- ae2:printed_calculation_processor
- ae2:printed_engineering_processor
- ae2:silicon
---

# Процессоры

<Row>
  <ItemImage id="logic_processor" scale="4" />
  <ItemImage id="calculation_processor" scale="4" />
  <ItemImage id="engineering_processor" scale="4" />
</Row>

Процессоры — один из основных ингредиентов для [устройств](../ae2-mechanics/devices.md) и машин AE2. Они также представляют одну из первых больших задач автоматизации. Существует три типа процессоров, создаваемых с использованием золота, <ItemLink id="certus_quartz_crystal" /> и алмаза соответственно. Они изготавливаются с помощью [клише](presses.md) в <ItemLink id="inscriber" /> в многоступенчатом процессе (обычно реализуемом через серию инскрайберов и фильтрованные трубопроводы).

## Этапы производства

<Column gap="5">
  1. Соберите/изготовьте необходимые ингредиенты: кремний, редстоун, золото, <ItemLink id="certus_quartz_crystal" />, алмаз.

  <RecipeFor id="silicon" />

  <br />

  2. Создайте предварительные печатные компоненты схем.

  <Row>
    <RecipeFor id="printed_silicon" />
    <RecipeFor id="printed_logic_processor" />
  </Row>
  <Row>
    <RecipeFor id="printed_calculation_processor" />
    <RecipeFor id="printed_engineering_processor" />
  </Row>

  <br />

  3. Финальная сборка.

  <Row>
    <RecipeFor id="logic_processor" />
    <RecipeFor id="calculation_processor" />
  </Row>
  <RecipeFor id="engineering_processor" />
</Column>