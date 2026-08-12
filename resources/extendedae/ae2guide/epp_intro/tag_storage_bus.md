---
navigation:
    parent: epp_intro/epp_intro-index.md
    title: МЭ Шина хранения по тегам
    icon: extendedae:tag_storage_bus
categories:
- extended devices
item_ids:
- extendedae:tag_storage_bus
---

# МЭ Шина хранения по тегам

<GameScene zoom="8" background="transparent">
  <ImportStructure src="../structure/cable_tag_storage_bus.snbt"></ImportStructure>
</GameScene>

МЭ Шина хранения по тегам — это <ItemLink id="ae2:storage_bus" />, которую можно настроить на фильтрацию по тегам предметов или жидкостей с поддержкой базовых логических операций.

Примеры:

- Принимать только необработанные руды:

`c:raw_materials`

- Принимать все слитки и драгоценные камни:

`c:ingots/* | c:gems/*`