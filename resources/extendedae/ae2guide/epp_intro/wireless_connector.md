---
navigation:
    parent: epp_intro/epp_intro-index.md
    title: МЭ Беспроводной соединитель
    icon: extendedae:wireless_connect
categories:
- extended devices
item_ids:
- extendedae:wireless_connect
- extendedae:wireless_tool
---

# МЭ Беспроводной соединитель

<Row gap="20">
<BlockImage id="extendedae:wireless_connect" scale="6"></BlockImage>
<ItemImage id="extendedae:wireless_tool" scale="6"></ItemImage>
</Row>

МЭ Беспроводной соединитель может связывать две сети, подобно <ItemLink id="ae2:quantum_link" />, но с ограничением по расстоянию и без возможности соединения через разные измерения.

## Соединение беспроводных соединителей

Щёлкните по двум беспроводным соединителям, которые вы хотите связать, с помощью <ItemLink id="extendedae:wireless_tool" />, чтобы установить соединение.

Присядьте и щёлкните, чтобы сбросить текущие настройки <ItemLink id="extendedae:wireless_tool" />.

МЭ Беспроводной соединитель изменит свою текстуру при успешном установлении связи.

Несоединённые МЭ Беспроводные соединители:

<GameScene zoom="5" background="transparent">
  <ImportStructure src="../structure/wireless_connector_off.snbt"></ImportStructure>
</GameScene>

Соединённые МЭ Беспроводные соединители:

<GameScene zoom="5" background="transparent">
  <ImportStructure src="../structure/wireless_connector_on.snbt"></ImportStructure>
</GameScene>

## Цвет

Беспроводные соединители можно окрашивать, как кабели, и они соединяются только с кабелями или соединителями того же цвета.

Для окрашивания соединителя используйте <ItemLink id="ae2:color_applicator" />.

Таким образом, вы можете настроить свои беспроводные соединители следующим образом:

<GameScene zoom="3" background="transparent" interactive={true}>
  <ImportStructure src="../structure/wireless_connector_setup.snbt"></ImportStructure>
</GameScene>

## Потребление энергии

МЭ Беспроводной соединитель потребляет больше энергии при увеличении расстояния между соединителями. Зависимость энергопотребления от расстояния нелинейна, поэтому затраты могут стать очень высокими при большом расстоянии.

Используйте <ItemLink id="ae2:energy_card" />, чтобы снизить энергопотребление; каждая карта уменьшает затраты энергии на 10%.