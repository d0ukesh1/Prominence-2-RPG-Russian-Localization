---
navigation:
  parent: items-blocks-machines-index.md
  title: МЭ интерфейс
  icon: interface
  position: 210
categories:
- devices
item_ids:
- ae2:interface
- ae2:cable_interface
---

# МЭ интерфейс

<Row gap="20">
<BlockImage id="interface" scale="8" />
<GameScene zoom="8" background="transparent">
  <ImportStructure src="../assets/blocks/cable_interface.snbt" />
</GameScene>
</Row>

МЭ интерфейсы действуют как небольшой сундук и резервуар для жидкостей, который заполняется из и опустошается в [сетевое хранилище](../ae2-mechanics/import-export-storage.md) в зависимости от того, что вы настроили для хранения в его слотах. Он пытается выполнить это за один игровой такт, поэтому может заполнить или опустошить до 9 стопок за такт, что делает его быстрым способом импорта или экспорта при наличии быстрых труб для предметов.

Ещё одно полезное свойство — в отличие от большинства резервуаров для жидкостей, которые могут хранить только один тип жидкости, интерфейсы могут хранить до 9 типов, а также предметы. По сути, это сундуки/многоцелевые резервуары с дополнительной функциональностью, и вы можете отключить эту функциональность, оставив их неподключёнными к сетям. Таким образом, они полезны в некоторых нишевых случаях, когда нужно хранить небольшое количество разных вещей.

## Как работает МЭ интерфейс внутри

Как уже сказано, МЭ интерфейс — это, по сути, сундук/резервуар с прикреплёнными супербыстрыми <ItemLink id="import_bus" /> и <ItemLink id="export_bus" />, а также множеством <ItemLink id="level_emitter" />.

<GameScene zoom="3" interactive={true}>
  <ImportStructure src="../assets/assemblies/interface_internals.snbt" />
  <BoxAnnotation color="#dddddd" min="1.3 0.3 1.3" max="9.7 1 1.7">
        Множество излучателей уровня для контроля запрашиваемого количества
        <GameScene zoom="4" background="transparent">
        <ImportStructure src="../assets/blocks/level_emitter.snbt" />
        </GameScene>
  </BoxAnnotation>
  <BoxAnnotation color="#dddddd" min="1.3 4 1.3" max="9.7 4.7 1.7">
        Множество излучателей уровня для контроля запрашиваемого количества
        <GameScene zoom="4" background="transparent">
        <ImportStructure src="../assets/blocks/level_emitter.snbt" />
        </GameScene>
  </BoxAnnotation>
  <BoxAnnotation color="#dddddd" min="1.3 1.3 1.3" max="9.7 2 1.7">
        Множество супербыстрых шин импорта, которые могут передавать 1 стопку за игровой такт
        <GameScene zoom="4" background="transparent">
        <ImportStructure src="../assets/blocks/import_bus.snbt" />
        </GameScene>
  </BoxAnnotation>
  <BoxAnnotation color="#dddddd" min="1.3 3 1.3" max="9.7 3.7 1.7">
        Множество супербыстрых шин экспорта, которые могут передавать 1 стопку за игровой такт
        <GameScene zoom="4" background="transparent">
        <ImportStructure src="../assets/blocks/export_bus.snbt" />
        </GameScene>
  </BoxAnnotation>
  <BoxAnnotation color="#dddddd" min="1 2 1" max="10 3 2">
        9 отдельных внутренних слотов
  </BoxAnnotation>
  <IsometricCamera yaw="195" pitch="15" />
</GameScene>

## Специальные взаимодействия

МЭ интерфейсы также имеют несколько особых функций с другими [устройствами](../ae2-mechanics/devices.md) AE2:

<ItemLink id="storage_bus" /> на ненастроенном интерфейсе предоставляет всё [сетевое хранилище](../ae2-mechanics/import-export-storage.md) своей сети сети МЭ шины хранения, как если бы сеть интерфейса была одним большим сундуком, на который установлена МЭ шина хранения. Настройка предметов для хранения в слотах фильтра интерфейса отключает эту функцию.

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/interface_storage.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

МЭ поставщики шаблонов имеют особое взаимодействие с интерфейсами в [подсетях](../ae2-mechanics/subnetworks.md): если интерфейс не настроен, поставщик шаблонов пропускает интерфейс и отправляет данные напрямую в [хранилище](../ae2-mechanics/import-export-storage.md) подсети, не заполняя интерфейс партиями рецептов и, что более важно, не вставляя следующую партию, пока в хранилище не появится место.

<GameScene zoom="6" background="transparent">
<ImportStructure src="../assets/assemblies/provider_interface_storage.snbt" />
<BoxAnnotation color="#dddddd" min="2.7 0 1" max="3 1 2">
        Интерфейс (должен быть плоским, не полным блоком)
  </BoxAnnotation>
<BoxAnnotation color="#dddddd" min="1 0 0" max="1.3 1 4">
        МЭ шины хранения
  </BoxAnnotation>
<BoxAnnotation color="#dddddd" min="0 0 0" max="1 1 4">
        Места, куда вы хотите подавать шаблоны (несколько машин или несколько сторон одной машины)
  </BoxAnnotation>
<IsometricCamera yaw="185" pitch="30" />
</GameScene>

## Варианты

МЭ интерфейсы бывают двух вариантов: обычный и плоский/[субкомпонент](../ae2-mechanics/cable-subparts.md). Это влияет на то, с каких сторон можно получить доступ к их инвентарю и обеспечивать сетевое соединение.

* Обычные интерфейсы позволяют вставлять, извлекать и получать доступ к инвентарю со всех сторон и, как большинство машин AE2, действуют как кабель, обеспечивая сетевое соединение со всех сторон.
* Плоские интерфейсы являются [субкомпонентами кабеля](../ae2-mechanics/cable-subparts.md), поэтому несколько таких интерфейсов можно разместить на одном кабеле, что позволяет создавать компактные установки. Они позволяют вставлять, извлекать и получать доступ к инвентарю с лицевой стороны, но не обеспечивают сетевое соединение через эту сторону.

МЭ интерфейсы можно переключать между обычным и плоским в сетке крафта.

## Настройки

Верхние слоты интерфейса определяют, что он должен хранить внутри себя. Когда что-то помещено в них или перетащено из JEI/REI, появляется гаечный ключ, позволяющий установить количество.

ПКМ с контейнером для жидкости (например, ведром или резервуаром для жидкости) установит эту жидкость как фильтр вместо предмета ведра или резервуара.

## Улучшения

МЭ интерфейс поддерживает следующие [улучшения](upgrade_cards.md):

* <ItemLink id="fuzzy_card" /> позволяет фильтровать по уровню повреждения и/или игнорировать NBT предметов.
* <ItemLink id="crafting_card" /> позволяет интерфейсу отправлять запросы на крафт в вашу систему [автокрафта](../ae2-mechanics/autocrafting.md) для получения нужных предметов. Он извлечёт предметы из хранилища, если они есть, прежде чем запрашивать создание нового предмета.

## Приоритет

Приоритеты можно установить, щёлкнув по гаечному ключу в правом верхнем углу интерфейса. Интерфейсы с более высоким приоритетом получат предметы раньше, чем те, у которых приоритет ниже.

## Рецепты

<Row>
  <Recipe id="network/blocks/interfaces_interface" />
  <RecipeFor id="cable_interface" />
</Row>