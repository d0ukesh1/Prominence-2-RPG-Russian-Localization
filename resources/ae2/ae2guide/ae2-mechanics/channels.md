---
navigation:
  parent: ae2-mechanics/ae2-mechanics-index.md
  title: Каналы
  icon: controller
---

# Каналы

МЭ-сети Applied Energistics 2 требуют каналы для поддержки [устройств](../ae2-mechanics/devices.md), использующих сетевое хранилище или другие сетевые службы. Представьте каналы как USB-кабели для всех ваших устройств. У компьютера только определённое количество USB-портов, и он может поддерживать только ограниченное число подключённых устройств. Большинство машин, полноразмерных устройств и стандартных кабелей могут передавать до 8 каналов. Можно представить полноразмерные устройства и стандартные кабели как пучок из 8 "проводов каналов". Однако [плотные кабели](../items-blocks-machines/cables.md#dense-cable) могут поддерживать до 32 каналов. Другие устройства, способные передавать 32 канала, — это <ItemLink id="me_p2p_tunnel" /> и [Квантовый мост](../items-blocks-machines/quantum_bridge.md). Каждый раз, когда устройство использует канал, представьте, что вы отсоединяете один "провод" из пучка, что, очевидно, означает, что этот "провод" недоступен дальше по линии.

<GameScene zoom="7" interactive={true}>
  <ImportStructure src="../assets/assemblies/channel_demonstration_1.snbt" />

  <LineAnnotation color="#33ff33" from="1 .4 .7" to="2.4 .4 .7" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .6 .7" to="2.4 .6 .7" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .4 .6" to="2.6 .4 .6" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .6 .6" to="2.6 .6 .6" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .6 .6" to="2.6 .6 .6" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="2.4 .6 .7" to="2.4 .6 1.5" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="2.4 .4 .7" to="2.4 .4 1.5" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="2.6 .6 .6" to="2.6 .6 1.5" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="2.6 .4 .6" to="2.6 .4 1.5" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="2.1 .6 1.5" to="2.4 .6 1.5" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="2.6 .4 1.5" to="2.9 .4 1.5" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="2.6 .6 1.5" to="2.6 .9 1.5" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="2.4 .1 1.5" to="2.4 .4 1.5" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="1 .6 .4" to="3.5 .6 .4" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .4 .4" to="3.5 .4 .4" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="3.5 .6 .4" to="3.5 .9 .4" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="3.5 .1 .4" to="3.5 .4 .4" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="1 .6 .3" to="1.5 .6 .3" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1 .4 .3" to="1.5 .4 .3" alwaysOnTop={true}/>

  <LineAnnotation color="#33ff33" from="1.5 .6 .3" to="1.5 .9 .3" alwaysOnTop={true}/>
  <LineAnnotation color="#33ff33" from="1.5 .1 .3" to="1.5 .4 .3" alwaysOnTop={true}/>

  <LineAnnotation color="#ff3333" from="3.5 .5 .5" to="5.5 .5 .5" alwaysOnTop={true}>
  Все 8 каналов в кабеле использованы, поэтому МЭ-дисковод не получает канал.  
  </LineAnnotation>

  <LineAnnotation color="#993333" from="1 .5 .5" to="1.25 .5 .5" alwaysOnTop={true}/>
  <LineAnnotation color="#993333" from="1.5 .5 .5" to="1.75 .5 .5" alwaysOnTop={true}/>
  <LineAnnotation color="#993333" from="2 .5 .5" to="2.25 .5 .5" alwaysOnTop={true}/>
  <LineAnnotation color="#993333" from="2.5 .5 .5" to="2.75 .5 .5" alwaysOnTop={true}/>
  <LineAnnotation color="#993333" from="3 .5 .5" to="3.25 .5 .5" alwaysOnTop={true}/>

  <DiamondAnnotation pos="3.6 0.5 0.5" color="#ff0000">
        Все 8 каналов в кабеле использованы, поэтому МЭ-дисковод не получает канал.
    </DiamondAnnotation>

  <IsometricCamera yaw="15" pitch="30" />
</GameScene>

Простой способ увидеть, как используются и направляются каналы в вашей сети, — использовать [умные кабели](../items-blocks-machines/cables.md), которые показывают пути и использование каналов.

Каналы потребляют 1⁄128 AE/тик за каждый узел, который они проходят. Это означает, что добавление <ItemLink id="controller" /> для сети с 8 устройствами и более чем 96 узлами может фактически снизить энергопотребление, поскольку изменяется способ распределения каналов.

Обратите внимание: **КАНАЛЫ НЕ ИМЕЮТ НИЧЕГО ОБЩЕГО С ЦВЕТОМ КАБЕЛЯ**, цвет кабеля лишь предотвращает их соединение.

## Маршрутизация каналов

При использовании <ItemLink id="controller" /> каналы направляются в три этапа. Сначала они выбирают кратчайший путь через соседние машины к ближайшему [обычному кабелю](../items-blocks-machines/cables.md) (стеклянному, покрытому или умному). Затем они выбирают кратчайший путь через этот обычный кабель к ближайшему [плотному кабелю](../items-blocks-machines/cables.md) (плотному или плотному умному). Затем они выбирают кратчайший путь через плотный кабель к <ItemLink id="controller" />. Если кратчайший путь уже полностью загружен, некоторые [устройства](devices.md) могут не получить нужные каналы. Используйте цветные кабели, кабельные якоря и туннели, чтобы направить каналы по желаемому пути.

Например, в этом случае некоторые МЭ-дисководы не получают каналы, потому что, хотя в кабелях достаточно пропускной способности, каналы пытаются выбрать кратчайший путь, перегружая одни кабели и оставляя другие пустыми.

<GameScene zoom="4" interactive={true}>
  <ImportStructure src="../assets/assemblies/channel_path_length_issue.snbt" />

  <LineAnnotation color="#33ff33" from="3 .5 1.4" to="0.4 0.5 1.4" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="0.4 .5 1.4" to="0.4 0.5 3.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="0.4 0.5 3.6" to="1.4 0.5 3.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="1.4 0.5 3.6" to="1.4 0.5 5" alwaysOnTop={true} thickness="0.05"/>

  <LineAnnotation color="#33ff33" from="3 0.5 3.6" to="1.6 0.5 3.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="1.6 0.5 3.6" to="1.6 0.5 5" alwaysOnTop={true} thickness="0.05"/>

  <LineAnnotation color="#ff3333" from="3 .5 1.6" to="0.6 .5 1.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#ff3333" from="0.6 .5 1.6" to="0.6 .5 3.4" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#ff3333" from="0.6 .5 3.4" to="1.4 .5 3.4" alwaysOnTop={true} thickness="0.05"/>

  <LineAnnotation color="#ff3333" from="3 .5 3.4" to="1.6 .5 3.4" alwaysOnTop={true} thickness="0.05"/>

  <BoxAnnotation color="#dddddd" min="1.2 0.2 3.2" max="1.8 0.8 3.8" alwaysOnTop={true} thickness="0.05">
        Здесь пытаются пройти более 8 каналов, поэтому некоторые обрезаются.
  </BoxAnnotation>

  <IsometricCamera yaw="90" pitch="90" />
</GameScene>

Это можно исправить, более тщательно ограничивая пути, по которым могут проходить каналы. Сети должны быть древовидными (или кустовидными). Петли и неоднозначные пути каналов следует минимизировать.

<GameScene zoom="4" interactive={true}>
  <ImportStructure src="../assets/assemblies/channel_path_length_issue_fix.snbt" />

  <LineAnnotation color="#33ff33" from="3 .5 1.4" to="0.4 0.5 1.4" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="0.4 .5 1.4" to="0.4 0.5 5.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="0.4 0.5 5.6" to="1 0.5 5.6" alwaysOnTop={true} thickness="0.05"/>

  <LineAnnotation color="#33ff33" from="3 0.5 3.6" to="1.6 0.5 3.6" alwaysOnTop={true} thickness="0.05"/>
  <LineAnnotation color="#33ff33" from="1.6 0.5 3.6" to="1.6 0.5 5" alwaysOnTop={true} thickness="0.05"/>

  <IsometricCamera yaw="90" pitch="90" />
</GameScene>

## Сети без МЭ-регулятора

Сеть без <ItemLink id="controller" /> считается временной и может поддерживать до 8 устройств, использующих каналы. Если вы превысите 8 устройств, устройства, использующие каналы, отключатся. Вы можете либо убрать устройства, либо добавить <ItemLink id="controller" />.

В отличие от сетей с МЭ-регулятором, [умные кабели](../items-blocks-machines/cables.md) во временных сетях показывают общее количество используемых каналов по всей сети, а не количество каналов, проходящих через конкретный кабель.

Временные сети используют по 1 каналу на устройство по всей сети, что сильно отличается от того, как <ItemLink id="controller" /> распределяет каналы по кратчайшему маршруту.

## Дизайн

Как упоминалось ранее в разделе [маршрутизация каналов](channels.md#channel-routing), лучше проектировать сеть в виде древовидной структуры, с плотными кабелями, отходящими от МЭ-регулятора, обычными кабелями, отходящими от плотных, и [устройствами](../ae2-mechanics/devices.md) в группах по 8 или меньше на обычных кабелях.

Вот пример того, чего делать не стоит:

Следуя путям каналов:

1. Сразу после выхода из МЭ-регулятора вправо мы ограничены 8 каналами, потому что МЭ-дисковод действует как обычный кабель. Однако, поскольку здесь не используется умный кабель, мы не видим, сколько каналов используется. Осталось 8 каналов.
2. МЭ-дисковод занимает один канал. Осталось 7 каналов.
3. 2 канала идут вверх к терминалам. Осталось 5 каналов.
4. Продолжая вправо, МЭ-интерфейс занимает ещё один канал. Осталось 4 канала.
5. 1 канал идёт вверх к МЭ поставщику шаблонов. Осталось 3 канала.
6. Продолжая вправо, 1 канал идёт вверх к МЭ шине импорта. Осталось 2 канала.
7. Группа МЭ поставщиков шаблонов, питающих сборщики, получает только 2 канала, поэтому 2 поставщика не получают каналы.

В конечном итоге ошибка заключается в ограничении каналов и непродуманном распределении каналов.

<GameScene zoom="4" interactive={true}>
  <ImportStructure src="../assets/assemblies/bad_network_structure.snbt" />

<LineAnnotation color="#33ff33" from="6.5 .5 1.5" to="6 .5 1.5" alwaysOnTop={true} thickness="0.4">
  32 канала
</LineAnnotation>

<LineAnnotation color="#33ff33" from="6 .5 1.5" to="5.5 .5 1.5" alwaysOnTop={true} thickness="0.2">
  8 каналов
</LineAnnotation>

<LineAnnotation color="#33ff33" from="5.5 .5 1.5" to="5.5 1.5 1.5" alwaysOnTop={true} thickness="0.1">
  2 канала
</LineAnnotation>

<LineAnnotation color="#33ff33" from="5.5 .5 1.5" to="5.5 .3 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="5.5 1.5 1.5" to="5.5 2.5 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="5.5 2.5 1.5" to="5.5 2.5 1.1" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="5.5 .5 1.5" to="4.5 .5 1.5" alwaysOnTop={true} thickness="0.158">
  5 каналов
</LineAnnotation>

<LineAnnotation color="#33ff33" from="4.5 .5 1.5" to="4.5 .3 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="4.5 .5 1.5" to="4.5 1.5 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="4.5 .5 1.5" to="3.5 .5 1.5" alwaysOnTop={true} thickness="0.122">
  3 канала
</LineAnnotation>

<LineAnnotation color="#33ff33" from="3.5 .5 1.5" to="3.5 2.5 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="3.5 2.5 1.5" to="3.7 2.5 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="3.5 .5 1.5" to="1.5 .5 1.5" alwaysOnTop={true} thickness="0.1">
  2 канала
</LineAnnotation>

<LineAnnotation color="#33ff33" from="1.5 0.5 1.5" to="1.5 0.3 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="1.5 0.5 1.5" to="0.5 0.5 1.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#33ff33" from="0.5 0.5 1.5" to="0.5 0.5 0.5" alwaysOnTop={true} thickness="0.071">
  1 канал
</LineAnnotation>

<LineAnnotation color="#ff3333" from="0.5 1.5 1.5" to="0.5 1.3 1.5" alwaysOnTop={true} thickness="0.071">
  Нет каналов
</LineAnnotation>

<LineAnnotation color="#ff3333" from="1.5 1.5 0.5" to="1.5 1.3 0.5" alwaysOnTop={true} thickness="0.071">
  Нет каналов
</LineAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

---

Вот пример хорошей структуры:

<GameScene zoom="2.5" interactive={true}>
  <ImportStructure src="../assets/assemblies/treelike_network_structure.snbt" />

    <BoxAnnotation color="#dddddd" min="6.9 0 4.9" max="9.1 4 7.1" thickness="0.05">
        Обратите внимание, что МЭ поставщики шаблонов разделены на группы по 8.
    </BoxAnnotation>

    <BoxAnnotation color="#dddddd" min="5 4 4" max="8 5 5" thickness="0.05">
        Два обычных кабеля, полных каналов, сходятся вместе, поэтому нужен плотный кабель.
    </BoxAnnotation>

    <BoxAnnotation color="#dddddd" min="5 0 13" max="8 1 14" thickness="0.05">
        Разные цвета кабелей используются, чтобы предотвратить соединение соседних кабелей.
    </BoxAnnotation>

  <IsometricCamera yaw="315" pitch="30" />
</GameScene>

## Режимы каналов

AE2 10.0.0 для Minecraft 1.18 вводит новые опции для изменения поведения каналов в вашем мире. В разделе общих настроек (`channels`) появилась новая конфигурационная опция, а также новая внутриигровая команда для операторов, позволяющая изменять режим и конфигурацию прямо в игре. Команда `/ae2 channelmode <mode>` изменяет режим, а `/ae2 channelmode` показывает текущий режим. При изменении режима в игре все существующие сети перезагрузятся и сразу начнут использовать новый режим.

Это возрождает и улучшает опцию, доступную в Minecraft 1.12, и предлагает лучшие варианты для игроков, которые хотят более расслабленный геймплей, но не желают полностью убирать эту механику.

В следующей таблице перечислены доступные режимы в конфигурационном файле и команде.

| Настройка  | Описание                                                                                                                                                                                                                               |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `default`  | Стандартный режим с пропускной способностью каналов для кабелей и временных сетей, как описано на этом сайте.                                                                                                                           |
| `x2`       | Все пропускные способности каналов удваиваются (16 на обычном кабеле, 64 на плотном кабеле, временные сети поддерживают 16 каналов).                                                                                                                           |
| `x3`       | Все пропускные способности каналов утраиваются (24 на обычном кабеле, 92 на плотном кабеле, временные сети поддерживают 24 канала).                                                                                                                           |
| `x4`       | Все пропускные способности каналов учетверяются (32 на обычном кабеле, 128 на плотном кабеле, временные сети поддерживают 32 канала).                                                                                                                       |
| `infinite` | Все ограничения на каналы снимаются. МЭ-регуляторы всё ещё значительно снижают энергопотребление сетей. Умные кабели будут переключаться только между полностью выключенным (без каналов) и полностью включённым (1 или более каналов). |