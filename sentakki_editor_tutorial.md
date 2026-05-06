## sentakki Beatmap Editor
The sentakki Editor is an UI-based maimai chart creation tool designed for use in sentakki. 
> [!WARNING]  
> Sentakki cannot save your content. Everything you design will be deleted as soon as you close the editor. Related: https://github.com/ppy/osu/issues/11736, https://github.com/LumpBloom7/sentakki/issues/791
<img width="1920" height="1080" alt="osu_2026-05-06_11-56-55" src="https://github.com/user-attachments/assets/92ffdc86-434d-4528-b9b2-092c5a263c02" />


## Interface
The interface of the editor follows the standard osu!lazer interface. 
 - The toolbox and toggles are located on the left side of the screen.
 - The inspection tab is located on the right side.

All other [metadata](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#metadata) properties (set in the "Setup" tab) and [timing](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#timing-points) properties (set in the "Timing" tab) adhere to other official osu! editors.

## Toolbox
The toolbox houses all of the note types from sentakki:
- Select (keybind: <kbd>1</kbd>): select a note from the ring using your cursor.
- [Taps](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#taps) (keybind: <kbd>2</kbd>).
- [Holds](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#holds) (keybind: <kbd>3</kbd>).
- [Slides](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#slides) (keybind: <kbd>4</kbd>).
- [Touch](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touch) (keybind: <kbd>5</kbd>).
- [TouchHold](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touchholds) (keybind: <kbd>6</kbd>).

## Toggles
Sentakki features, along the regular [hitsounding options](https://osu.ppy.sh/wiki/en/Beatmapping/Hitsound), two behavioural modifiers:

- [Break](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#break-modifier) (keybind: <kbd>R</kbd>): increases the scoring weight of notes. Typically used to emphasize certain notes, or to increase punishment for innacuracy.
- [Ex](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#ex-modifier) (keybind: <kbd>T</kbd>): Increases the judgement leniency of notes. Typically used to provide a safety net for players, allowing harder patterns to be introduced, or to emphasize "dilluted" musical notes.

All objects can have both the `Break` and `Ex` modifier applied to them, except for `TouchHold`s which can only can have the `Break` modifier.

## Inspector
The inspection tool allows the user to view precise information about the selected note, such as its position, time or modifiers.
Most of the options from the `Inspector` tool can be directly altered by left clicking on the text.

## Slide Creation
To start the slide creation process, select the `Slide` button in the Toolbox and place the slide on one of the avalable lanes.
- Identify a shape you wish to place by moving your mouse around the eight avalable lanes. If none of the avalable options are satisfactory, you can press <kbd>Alt-LClick</kbd> to mirror your shape in the other direction, or by using <kbd>Tab</kbd> or <kbd>Alt-MWheel</kbd> if you wish to entirely change the selected slide shape.
- Once you find a satisfactory shape, press <kbd>LClick</kbd> to place your shape down. You may place multiple shapes in a single slide.
- Press <kbd>RClick</kbd> to place the Slide down.
- At the end, you can drag the dot located in the timeline to change the amount of time for which the `Slide` is visible. This works for `Touch`es and `TouchHold`s too.

## Slide Modification
There are two methods which you can use to change an already placed slide:
- Right Click: Select the Slide using left click and right click one of the shapes.
- Inspector: Select the Slide using left click and select a slide shape from the inspector menu (under `Segments:`).

Both methods feature the following options:
- Duplicate: Adds a clone of the previous shape to the end of the currrecntly selected shape.
- End Lane: Changes the end of the currently selected shape. The numbers match the [playfield lane number](https://w.atwiki.jp/simai/pages/1003.html#id_41f8fdb8).
- Delete/Delete Segment: Deletes the currently selected segment.

## Advanced Information
> [!NOTE]
> Changing some of these options could result in your map receiving an unofficial "Aspire" or "Utage" label.
- Touch Snap Grid (Accessible from the toolbox, or using the keybind <kbd>Y</kbd>): Snaps all touches to [valid simai sensors](https://w.atwiki.jp/simai/pages/1003.html#id_2e7f7388). Typically used for backwards compatibility.
- Slide Modifiers (accessibly by right clicking the slide body): Adds the Break or Ex modifiers directly to the Slide Body.
- Slide shoot offset (accessible by left clicking on the slide, navigating to its start and dragging the white dot, or with <kbd>+</kbd> and <kbd>-</kbd>): Changes the delay between the Slide Star landing on the ring and starting its movement.
- Omit Slide Tap (accessibly by right clicking the slide): Removes the star from the Slide.
- Hold note length manipulation: You can select a `Hold` note and drag the dots located within it to change its length. This also allows you to create zero length hold notes. `TouchHold`s do not support this functionality.
