# Charting/Mapping with sentakki
So now you installed the ruleset, with the aim of mapping something that represent **you**, but the lazer editor is too confusing. This wiki article aim to help you navigate the editor and start to create your own maps.
> Note: Simai is not supported in the release channel of sentakki, and so is saving.

## 1, The Interface
The interface is just a standard osu!lazer interface, but with some small modification. On the left panel, we have the toolbox, and the toggles. These will be our main focus.
<!--insert picture of left panel-->

And on the right side, we have the inspector. The inspector will show various data about an object, which we will go deep into it later.

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
Some of them even have tooltips, try to hover above the button to see what those are.

### 1.2: The Toggles
All the toggles work as the same as the base osu! editor, but there are four new toggles in sentakki. Two of the most important will be mentioned here, the other two will be in the [Advance Mapping]:

- [Break](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#break-modifier) (keybind: <kbd>R</kbd>): Apply the break modifier to the selected object(s) or make all the notes placed after activate to have break modifier.
- [Ex](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#ex-modifier) (keybind: <kbd>T</kbd>): Apply the ex modifier to the selected object(s) or make all the notes placed after activate to have ex modifier.

> Note: All of the objects can have both `Break` and `Ex` modifier applied to them, except for `Touchholds` only can have `Break` modifier.

> For the slides, only the slide tap will be affected by this toggle.
### 1.3: The Inspector
The inspector located on the right, where it will show you the various attribute of an object. All of them, however, will display the same a few key attributes:

- Type: Show what type of note it is (taps, holds, slides, touch or Touchhold).
- Modifier: Whether the object have the [modifier](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#modifiers) on them.
- Time: The timing of the object, count in milisecond relative to the start of the song.
<!-- Try to show all of them in one picture?-->

All the attribute below will only appear when select the corresponding object:
- Duration (only on Hold, Slide and Touchhold): show how long the object last in both milisecond and beat counts.
- Position`[x, y]` (only on touch and touchhold): show where the touch/touchhold on the screen, with the centre of the playfield equivalent to `x = 0` and `y = 0`.
- Position`[lane]`: show which [lane]() <!--need the link about lane, which is later in the playfield section. Remove this comment once the link is added--> is the object is located or started on.
- Wait duration (only on Slide): show how long the star will wait before shoot off.
- Movement duration (only on Slide): show how long the star will travel on the slide after shoot off.
- Segments (only on Slide): show how many segment of slides is on that slide. The syntax used there is `shape of slide(A number to show position relative to the last segment end)`
    > Note: The number shown is positive if the segment ended closest is in the clockwise position and negative  if the segment ended closest is in the counter-clockwise position
    <!-- The note need repharse -->
- Slide modifier: The slide body contain its own modifier, separate from the modifier of the slide tap. Slide body modifier will be shown here.
