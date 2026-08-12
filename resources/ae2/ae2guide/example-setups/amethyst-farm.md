---
navigation:
  parent: example-setups/example-setups-index.md
  title: Ферма аметистов
  icon: minecraft:amethyst_shard
---

# Ферма аметистов

Хотя <ItemLink id="growth_accelerator" /> (Ускоритель роста) работает с аметистами, обычные методы фильтрации [бутонов истинного кварца](../items-blocks-machines/budding_certus.md) с помощью <ItemLink id="annihilation_plane" /> (МЭ плоскости уничтожения) не работают с бутонами аметиста. В отличие от незрелых бутонов истинного кварца, которые дают <ItemLink id="certus_quartz_dust" /> (Пыль истинного кварца), незрелые бутоны аметиста не дают ничего, поэтому плоскость уничтожения всегда будет их разрушать, так как сеть может хранить «ничего».

Решение — зачаровать плоскость уничтожения на «Шёлковое касание». Тогда незрелые бутоны аметиста *действительно* дают что-то (разные стадии физических блоков бутонов), и их можно фильтровать.

<ItemLink id="minecraft:amethyst_cluster" /> (Друза аметиста) затем должна быть снова размещена с помощью <ItemLink id="formation_plane" /> (МЭ плоскости формирования), чтобы затем быть повторно разрушена <ItemLink id="annihilation_plane" /> (МЭ плоскостью уничтожения) без «Шёлкового касания» для получения <ItemLink id="minecraft:amethyst_shard" /> (Осколков аметиста).

Обратите внимание, что из-за направленности друзы напротив плоскости формирования должен быть сплошной блок.

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/assemblies/amethyst_farm.snbt" />

  <BoxAnnotation color="#dddddd" min="2.7 1 1" max="3 2 2">
        (1) МЭ плоскость уничтожения №1: Без интерфейса для настройки, но зачарована на «Шёлковое касание».
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="2 1 1" max="2.3 2 2">
        (2) МЭ плоскость формирования: Отфильтрована на Друзу аметиста.
        <ItemImage id="minecraft:amethyst_cluster" scale="2" />
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="1.3 0.7 1" max="2 1 2">
        (3) МЭ плоскость уничтожения №2: Без интерфейса для настройки, но может быть зачарована на «Удачу».
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="1 0 1" max="1.3 1 2">
        (4) МЭ шина хранения №1: Отфильтрована на Осколки аметиста.
        <ItemImage id="minecraft:amethyst_shard" scale="2" />
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="0 0 .7" max="1 1 1">
        (5) МЭ шина хранения №2: Отфильтрована на Осколки аметиста. Имеет приоритет выше, чем у основного хранилища.
        <ItemImage id="minecraft:amethyst_shard" scale="2" />
  </BoxAnnotation>

<DiamondAnnotation pos="0 0.5 0.5" color="#00ff00">
        К основной сети
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## Настройки

* Первая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) (1) не имеет интерфейса и не может быть настроена, но должна быть зачарована на «Шёлковое касание».
* <ItemLink id="formation_plane" /> (МЭ плоскость формирования) (2) отфильтрована на <ItemLink id="minecraft:amethyst_cluster" /> (Друзу аметиста).
* Вторая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) (3) не имеет интерфейса и не может быть настроена, но может быть зачарована на «Удачу».
* Первая <ItemLink id="storage_bus" /> (МЭ шина хранения) (4) отфильтрована на <ItemLink id="minecraft:amethyst_shard" /> (Осколки аметиста).
* Вторая <ItemLink id="storage_bus" /> (МЭ шина хранения) (5) отфильтрована на <ItemLink id="minecraft:amethyst_shard" /> (Осколки аметиста) и имеет [приоритет](../ae2-mechanics/import-export-storage.md#storage-priority) выше, чем у основного хранилища.

## Как это работает

1. Первая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) пытается разрушить то, что находится перед ней, но может разрушить только <ItemLink id="minecraft:amethyst_cluster" /> (Друзу аметиста), так как единственное хранилище в подсети — <ItemLink id="formation_plane" /> (МЭ плоскость формирования), отфильтрованная на друзу аметиста. Это работает только потому, что плоскость зачарована на «Шёлковое касание», иначе она могла бы разрушать незрелые бутоны, так как они не дают дропа.
2. <ItemLink id="formation_plane" /> (МЭ плоскость формирования) размещает друзу на блоке напротив неё.
3. Вторая <ItemLink id="annihilation_plane" /> (МЭ плоскость уничтожения) разрушает друзу, производя <ItemLink id="minecraft:amethyst_shard" /> (Осколки аметиста).
4. Первая <ItemLink id="storage_bus" /> (МЭ шина хранения) сохраняет осколки в бочку. Технически её не обязательно фильтровать, так как вторая плоскость уничтожения должна сталкиваться только с полностью выросшими друзами.
5. Вторая <ItemLink id="storage_bus" /> (МЭ шина хранения) предоставляет основной сети доступ ко всем осколкам аметиста в бочке. Она настроена на высокий [приоритет](../ae2-mechanics/import-export-storage.md#storage-priority), чтобы осколки аметиста предпочтительно возвращались в бочку, а не в основное хранилище.