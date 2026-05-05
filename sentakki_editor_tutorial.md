## Sentakki Beatmap Editor
The sentakki Editor is an UI-based maimai chart creation tool designed for use in sentakki. 
> [!WARNING]  
> Sentakki cannot save your content. Everything you design will be deleted as soon as you close the editor. Related: https://github.com/ppy/osu/issues/11736, https://github.com/LumpBloom7/sentakki/issues/791


## The Interface
The interface of the editor follows the standard osu!lazer interface. 
 - The toolbox, toggles and bank options are located on the left side of the screen.
 - The inspection tab is located on the right side.

All other [metadata](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#metadata) properties (set in the "Setup" tab) and [timing](https://osu.ppy.sh/wiki/en/Client/File_formats/osu_(file_format)#timing-points) properties (set in the "Timing" tab) adhere to other official osu! editors.

## Toolbox
The Toolbox house all the objects there are in sentakki:
- Select: select a note from the ring using your cursor.
- [Taps](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#taps) (keybind: <kbd>2</kbd>).
- [Holds](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#holds) (keybind: <kbd>3</kbd>).
- [Slides](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#slides) (keybind: <kbd>4</kbd>).
- [Touch](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touch) (keybind: <kbd>5</kbd>).
- [TouchHold](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#touchholds) (keybind: <kbd>6</kbd>).

## Toggles
Sentakki features, along the regular [hitsounding options](https://osu.ppy.sh/wiki/en/Beatmapping/Hitsound), two behavioural modifiers and two grid snap toggles.

- [Break](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#break-modifier) (keybind: <kbd>R</kbd>): increases the scoring weight of notes. Typically used to emphasize certain notes, or to increase punishment for innacuracy.
- [Ex](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#ex-modifier) (keybind: <kbd>T</kbd>): Increases the judgement leniency of notes. Typically used to provide a safety net for players, allowing harder patterns to be introduced, or to emphasize "dilluted" musical notes.
- Lane Note Snap Grid (keybind: <kbd>Y</kbd>): Toggle timeline-based [Beat Snap](https://osu.ppy.sh/wiki/en/Beatmapping/Beat_snapping).
- Touch Snap Grid (keybind: <kbd>U</kbd>): Snaps all touches to [valid simai sensors](https://w.atwiki.jp/simai/pages/1003.html#id_2e7f7388). Typically used for backwards compatibility.

All objects can have both the `Break` and `Ex` modifier applied to them, except for `TouchHold`s which can only can have the `Break` modifier.

## Inspector
The inspection tool allows the user to view precise information about the selected note.

- Type: Shows the note type of the selected note (Tap, Hold, Slide, Touch or TouchHold).
- Modifier: Whether the selected object has [modifier](https://github.com/LumpBloom7/sentakki/wiki/Hit-Objects#modifiers) applied on them.
- Time: The position of the hit object in the timeline, displayed in miliseconds relative to the start of the song.
- Position: Displays the sensor or coordonates of the selected note in the ring.

The attributes from below will only appear when the appropriate note type is selected:
- Duration (only on `Hold`, `Slide` and `TouchHold`): Shows how long the object lasts in miliseconds and beats.
- Wait duration (only on `Slide`): Shows how long the star will wait before its shoot off.
- Movement duration (only on `Slide`): Shows how long the star will travel on the slide after its shoot off.
- Segments (only on `Slide`): Displays all the segments added on the slide.
- Slide modifier: The Slide body contain its own modifier, separate from the modifier of the slide tap. Slide body modifier will be shown here.
Several options in the `Inspector` tool can be directly altered by left clicking on the text.

## Slide Creation
- To start the slide creation process, select the `Slide` button in the Toolbox and place the slide on one of the avalable lanes.
- Identify a shape you wish to place by moving your mouse around the eight avalable lanes. If none of the avalable options are satisfactory, you can press <kbd>Alt-LClick</kbd> to mirror your shape in the other direction, or by using <kbd>Tab</kbd> or <kbd>Alt-MWheel</kbd> if you wish to entirely change the selected slide shape.
- Once you find a satisfactory shape, press `LClick` to place your shape down. You may place multiple shapes of differing shapes and mirroring options.
- Press <kbd>RClick</kbd> to place the Slide down.
- Go to the start of the Slide and select the Slide. You can either select the white dot and move it or press <kbd>+</kbd> and <kbd>-</kbd> to change the delay between the slide landing and the slide starting its movement.
  - Warning: Changing this could result in your map receiving an "Aspire" or "Utage" label. If you wish to undo this, set the delay to one beat.

## Slide Modification
There are two methods which you can use to change an already placed slide:
- Right Click: Select the Slide using left click and right click one of the shapes.
  - Slide Modifiers: Adds the Break or Ex modifiers to the Slide Body.
  - Omit Slide Tap: Removes the Slide Star from the Slide. Does not remove the Shoot Offset by default.
    - Warning: Enabling this could result in your map receiving an "Aspire" or "Utage" label.
- Inspector: Select the Slide using left click and select a slide shape from the inspector menu (under `Segments:`).
Both methods feature the following options:
- Duplicate: Adds a clone of the previous shape to the end of the currrecntly selected shape.
- End Lane: Changes the end of the currently selected shape. The numbers match the [playfield lane number](https://w.atwiki.jp/simai/pages/1003.html#id_41f8fdb8).
- Delete/Delete Segment: Deletes the currently selected segment.
Additionally, you can select the end of the slide segment to directly change the end lane of the slide.
