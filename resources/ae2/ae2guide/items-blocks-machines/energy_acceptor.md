---
navigation:
  parent: items-blocks-machines-index.md
  title: МЭ приёмник энергии
  icon: energy_acceptor
  position: 110
categories:
- network infrastructure
item_ids:
- ae2:energy_acceptor
---

# МЭ приёмник энергии

<Row gap="3">
<BlockImage id="energy_acceptor" scale="4" /> 
<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/blocks/cable_energy_acceptor.snbt" />
</GameScene>
</Row>

МЭ приёмник энергии преобразует распространённые формы энергии из других технических модов во внутреннюю форму [энергии](../ae2-mechanics/energy.md) AE2, AE. Хотя <ItemLink id="controller" /> также может это делать, стороны регулятора ценны, поэтому часто лучше использовать МЭ приёмник энергии.

Коэффициенты преобразования для энергии Forge и энергии TechReborn:

* 2 FE = 1 AE (Forge)
* 1 E = 2 AE (Fabric)

Скорость преобразования полностью зависит от того, сколько AE может хранить ваша сеть, по причинам, описанным на [этой странице](../ae2-mechanics/energy.md).

## Варианты

МЭ приёмники энергии бывают двух вариантов: обычный и плоский/[субкомпонент](../ae2-mechanics/cable-subparts.md). Это позволяет делать некоторые установки более компактными.

МЭ приёмники энергии можно переключать между обычным и плоским в сетке крафта.

## Рецепты

<Row>
  <RecipeFor id="energy_acceptor" />
  <RecipeFor id="cable_energy_acceptor" />
</Row>