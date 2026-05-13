# Charting/Mapping with sentakki
**So now you installed the ruleset**, with the aim of mapping something that represent you, **but the lazer editor is too confusing**. This wiki article aim to help you navigate the editor and start to create your own maps.
> [!NOTE]
> Simai is not supported in the release channel of sentakki, and so is saving.

## 1, The Interface
The interface is just a standard osu!lazer interface, but with some modification, all of them are on the composer tab. On the left panel, we have the toolbox, and the toggles.
<!--insert picture of left panel-->

And on the right side, we have the inspector. The inspector will show various data about an object

<!--insert picture of right panel-->

All other [metadata](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#metadata) properties (set in the "Setup" tab) and [timing](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#timing-points) properties (set in the "Timing" tab) is adhere to the normal osu!

### 1.1: The Toolbox
The "Toolbox" house all the objects there are in sentakki:
- [Taps](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#taps) (keybind: <kbd>2</kbd>)
- [Holds](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#holds) (keybind: <kbd>3</kbd>)
- [Slides](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#slides) (keybind: <kbd>4</kbd>)
- [Touch](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touch) (keybind: <kbd>5</kbd>)
- [Touchhold](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touchholds) (keybind: <kbd>6</kbd>)

<!--Toolbox picture goes here-->
Some of them even have tooltips, mostly to provide shortcuts guidance that are applied to the current release.
### 1.2: The Toggles
All the toggles work as the same as the base osu! editor, but there are four new toggles in sentakki:

- [Break](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#break-modifier) (keybind: <kbd>R</kbd>): Apply the break modifier to the selected object(s) or make all the notes placed after activate to have break modifier.
- [Ex](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#ex-modifier) (keybind: <kbd>T</kbd>): Apply the ex modifier to the selected object(s) or make all the notes placed after activate to have ex modifier.
- Lane note snap grid (keybind: <kbd>Y</kbd>): This feature enable the timing snap grid visible after picking the type of object from the toolbox. Similar to the osu!mania timing grid
<!--only if this support gif, or I guess a simple picture can work-->
- Touch snap grid (keybind: <kbd>U</kbd>): Touch note will be snapped to the points which are visible after picking either touch or touchhold object from the toolbox. The position of the dots correspond to the centre of the sensor in the official maimai cabinet. See: [maimai sensor map](https://static.wikitide.net/argwwiki/6/61/Maimai_New_Sensor_Map.png)
> Note: All of the objects can have both `Break` and `Ex` modifier applied to them, except for `Touchholds` only can have `Break` modifier.

> For the slides, only the slide tap will be affected by the toggle.
### 1.3: The Inspector
The inspector located on the right, where it will show you the various attribute of an object. All of them, however, will display the same a few key attributes:

- Type: Show what type of note it is (taps, holds, slides, touch or Touchhold).
- Modifier: Whether the object have the [modifier](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#modifiers) on them.
- Time: The timing of the object, count in milisecond relative to the start of the song.
<!-- Try to show all of them in one picture?-->

All the attribute below will only appear when select the corresponding object:
- Duration (only on `Hold`, `Slide` and `Touchhold`): show how long the object last in both milisecond and beat counts.
- Position`[x, y]` (only on `Touch` and `Touchhold`): show where the touch/touchhold on the screen, with the centre of the playfield equivalent to `x = 0` and `y = 0`.
- Position`[lane]`: show which [lane]() <!--need the link about lane, which is later in the playfield section. Remove this comment once the link is added--> is the object is located or started on.
- Wait duration (only on `Slide`): show how long the star will wait before shoot off, measure in both milisecond and beat counts.
- Movement duration (only on `Slide`): show how long the star will travel on the slide after shoot off, measure in both milisecond and beat counts.
- Segments (only on `Slide`): show how many segment of slides is on that slide. The syntax used is `shape of slide(A number to show position relative to the last segment end)`
    > [!NOTE]
    > The number shown is positive if the segment ended closest is in the clockwise position and negative  if the segment ended closest is in the counter-clockwise position
    <!-- The note need repharse -->
- Slide modifier: The slide body contain its own modifier, separate from the modifier of the slide tap. Slide body modifier will be shown here.

Several attributes in the `Inspector` can be directly altered by left clicking on the text. It will highlight with yellow on hover if the attribute is modifiable.


> [!NOTE]
> All other element stays the same. You can find a guide/wiki [here]()<!--link of the original wiki on osu-->
## 2, The Playfield
In the middle of the main composer tab is the playfield. This playfield adhere to the [maimai interface](https://static.wikitide.net/argwwiki/6/61/Maimai_New_Sensor_Map.png)

### 2.1: The ring
The ring is the boundary of the playfield, and also the judgement lines for all the laned notes.


### 2.2: Lane and touch sensors:
These are the 8 fixed position on the ring for "lane" (sometime they also called sensors), separate by <!-- angel -->. Lanes note can accomodate non-touch objects (tap, hold and the slide tap).

The touches are distributed on the screen, with their centre formed a 3 circles formation and an extra touch sensor in the middle