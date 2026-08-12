---
navigation:
  parent: items-blocks-machines-index.md
  title: МЭ молекулярный сборщик
  icon: molecular_assembler
  position: 310
categories:
- machines
item_ids:
- ae2:molecular_assembler
---

# МЭ молекулярный сборщик

<BlockImage id="molecular_assembler" scale="8" />

МЭ молекулярный сборщик принимает предметы, поступающие в него, и выполняет операцию, заданную соседним <ItemLink id="pattern_provider" /> или вставленным <ItemLink id="crafting_pattern" />, <ItemLink id="smithing_table_pattern" /> или <ItemLink id="stonecutting_pattern" />, затем отправляет результат в соседние инвентари.

Этот сборщик имеет шаблон крафта, который определяет рецепт: 1 дубовое бревно = 4 дубовые доски. Когда дубовые брёвна поступают в верхнюю воронку, сборщик создаёт дубовые доски и отправляет их в нижнюю воронку.

<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/assemblies/standalone_assembler.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Основное применение молекулярного сборщика

Основное использование — рядом с <ItemLink id="pattern_provider" />. В этом случае МЭ поставщики шаблонов имеют особое поведение и отправляют информацию о соответствующем шаблоне вместе с ингредиентами в соседние сборщики. Поскольку сборщики автоматически выталкивают результаты крафта в соседние инвентари (и, следовательно, в слоты возврата МЭ поставщика шаблонов), сборщик на МЭ поставщике шаблонов — это всё, что нужно для автоматизации шаблонов крафта.

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/assembler_tower.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Улучшения

МЭ молекулярный сборщик поддерживает следующие [улучшения](upgrade_cards.md):

* <ItemLink id="speed_card" />

## Рецепт

<RecipeFor id="molecular_assembler" />

## Примечание

Optifine нарушает функцию "выталкивания в соседние инвентари", поэтому большинство установок крафта с молекулярными сборщиками не будут работать.