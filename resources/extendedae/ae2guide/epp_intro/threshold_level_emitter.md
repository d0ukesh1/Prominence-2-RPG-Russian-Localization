---
navigation:
    parent: epp_intro/epp_intro-index.md
    title: МЭ Пороговый излучатель уровня
    icon: extendedae:threshold_level_emitter
categories:
- extended devices
item_ids:
- extendedae:threshold_level_emitter
---

# МЭ Пороговый излучатель уровня

<GameScene zoom="8" background="transparent">
  <ImportStructure src="../structure/cable_threshold_level_emitter.snbt"></ImportStructure>
</GameScene>

Работает как триггер с двумя порогами. Он отключает сигнал редстоуна, если количество предмета в сети меньше нижнего порога, и включает сигнал, если количество превышает верхний порог.

Например, если нижний порог установлен на 100, а верхний — на 150:

Изначально сеть пуста, и излучатель не активен.

Когда количество предмета увеличивается и превышает 150, излучатель начинает подавать сигнал редстоуна.

Если количество уменьшается и становится меньше 150, излучатель продолжает подавать сигнал.

Когда количество падает ниже 100, излучатель отключается.