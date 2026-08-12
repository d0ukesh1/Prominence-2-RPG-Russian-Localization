---
navigation:
  parent: ae2-mechanics/ae2-mechanics-index.md
  title: Выращивание истинного кварца
  icon: quartz_cluster
---

# Выращивание истинного кварца

## В основном скопировано со страницы "Начало работы"

<GameScene zoom="6" background="transparent">
<ImportStructure src="../assets/assemblies/budding_certus_1.snbt" />
</GameScene>

Бутоны истинного кварца вырастают на [цветущих блоках истинного кварца](../items-blocks-machines/budding_certus.md), подобно аметисту. Если вы сломаете бутон, который ещё не полностью вырос, он даст одну <ItemLink id="certus_quartz_dust" />, и зачарование "Удача" на это не влияет. Если вы сломаете полностью выросшую друзу, она даст четыре <ItemLink id="certus_quartz_crystal" />, и зачарование "Удача" увеличит это количество.

Существует 4 уровня цветущих блоков истинного кварца: безупречный, потрескавшийся, треснувший и повреждённый.

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/budding_blocks.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Каждый раз, когда бутон вырастает на следующую стадию, цветущий блок может понизиться на один уровень, в конечном итоге превращаясь в обычный блок истинного кварца. Их можно восстановить (или создать новые цветущие блоки), поместив цветущий блок (или блок истинного кварца) в воду с одним или несколькими <ItemLink id="charged_certus_quartz_crystal" />.

<RecipeFor id="damaged_budding_quartz" />

Безупречные цветущие блоки истинного кварца не портятся и будут бесконечно производить истинный кварц. Однако их нельзя изготовить или переместить с помощью кирки, даже с "Шёлковым касанием". (Но их *можно* переместить с помощью [пространственного хранилища](../ae2-mechanics/spatial-io.md).)

Сами по себе бутоны истинного кварца растут очень медленно. К счастью, <ItemLink id="growth_accelerator" /> значительно ускоряет этот процесс, если разместить его рядом с цветущим блоком. Создание нескольких таких ускорителей должно быть вашим первым приоритетом.

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/assemblies/budding_certus_2.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

Если у вас недостаточно кварца для создания <ItemLink id="energy_acceptor" /> или <ItemLink id="vibration_chamber" />, вы можете изготовить <ItemLink id="crank" /> и установить его на конец ускорителя.

Автоматический сбор истинного кварца [описан здесь](../example-setups/simple-certus-farm.md).