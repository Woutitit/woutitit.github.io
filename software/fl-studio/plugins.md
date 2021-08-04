# Plugins
## Fruity Limiter
Purposes:
- Limting
- Compression

### How to add makeup gain
- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Fruity%20Limiter.htm

There is make up gain in Fruity Limiter. It's called gain, however, note that it's only makeup gain POST compressor but PRE limiter. However, usually this makes sense

## NewTone
> Also see "vocal production" article.

Purposes:
- Pitch correcting audio (e.g. vocal performances)
- Converting audio to MIDI
- Creating harmonies

Sources:
- https://www.image-line.com/fl-studio/plugins/newtone
- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Newtone.htm

### Basic use
1. Put NewTone on mixer FX channel
2. Drag a sample in the playlist
3. Open up NewTone
4. Drag and drop the sample in the NewTone playlist (You can also load a sample through File > Load sample)
5. Have fun!

### Pitch correcting audio (e.g. vocal performances)
#### Global pitch correction
Absolute most basic pitch correction is with the 3 knobs top right. Center especially will (if 100%) just correct the note to the nearest musical pitch. You may need to manually drag some corrected notes to the actual note you want after as the nearest note in pitch may not always be the note you wanted/needed there. Variation knob takes care of too much vibrato and the transition knob may tweak how fast it goes to a new pitch (i.e. too fast transition may sound unnatural, too slow may sound too bad vocal performance)

You can click the "Send to playlist" button if you're happy with the correction.

#### Note by note
Global pitch correction may be all you need but it has the least control and thus too much global correction may sound too unnatural for your taste (or it may not be enough). Individually snapping pitches can be done with right-click. And dragging pitches can be done if you click in the middle of the note and drag.

*Tip: the transparent block shows the nearest semitone. The bordered block the average pitch of the note. Therefore, the blocks where you see the most variance in there you'll probably want/need to correct the most.*

Then there is also the advanced menu you can access either with the advanced button or double clicking a note (to untoggle, click the pink button top right again). There you can again control the pitch, vibrato an

### Converting audio to MIDI
Sometimes you may want to analyze something or may want to have some audio in MIDI. What you can do is load up a VST, select it in the channel rack (i.e. needs to be green in the channel rack) and then click the "Send to piano roll" button and boom there you have it (not sure if it can do chords though).

### Creating harmonies
Since you can easily send audio to playlist you can send your original performance to playlist, you can then select everything and then move it up +3, +5, +12 or whatever you want and then send that to the playlist. You can even drag individual pitches to different pitches for even cooler counterpoint harmony very easily. And, you always keep you original sample in the playlist (muted) if you screw up too much.

## Transient processor
Purposes:
- Effectively and easily shaping transient and body of sound

Sources:
- https://www.image-line.com/fl-studio/plugins/transient-processor
- https://www.youtube.com/watch?v=3QpZYSUljmw&t=211s

### Description
Transient processor is kind of like a magic compressor though the attack doesn't have anything to do with how fast it kicks in and release also doesn't have to do with how fast it let's go. The attack simply magically kind of looks at the beginning attack/transient part of a sound and then you can spin the dial and literally just make that part louder or quieter so either making it less or more punchy. With the release knob, it looks more at the body/end of a sound and again you literally can pull it more up or put it more down depending on what you want or need. So yeah a bit like a saturator/compressor does. Not sure if saturation makes it even more fatter than just processing but with this you get a lot of control on how punchy and/or fat you want your stuff to sound like.

It seems that saturation still makes stuff fatter (if needed) but that you may be able to do TP before or after to add some more transient back in or even more punch in if needed but that you still want clipping/saturation for fatness (?).

Also, it even works on a synth INIT patch (so full sustain no attack no release) and it will give it some attack (I guess so in that case or all cases it looks at a certain amount in ms in the beginning and shapes that), however, the release didn't work because the stuff is flat and not dynamic at all and also the attack was also just a little thump and stuff. So again, transient shaper works best on synth patches, instruments (such as percussion and plucks) that have transients/dynamics/fading tail and thus are meant to be more stabb/percussive. So it's for transient-functional sounds to be enhanced and shaped even more in their transients.

## Patcher
Purposes:
- Saving instruments with all layers and post-processing included
- Parallel processing
- Visualization of FX chain

Patcher is a very handy tool that is there to improve and visualize your workflow and can be either used as an instrument or an effect. What you can do in Patcher is visually add VSTs, such as Serum, and then on top of that add all kinds of post-processing fx to it. Or, you can use it as an FX and you can route your signal through the patcher instance. 

So it's mostly handy for preset saving, flexibility in (advanced) sound design, and then for the visual and drag-and-droppy stuff for people that prefer to do stuff visually.

### Saving instruments with multiple layers and post-processing
It's very common that you have a certain sound that either comprises of multiple layers or has certain post-processing to make it the sound that it is. For example, check out the Mo Falk video, it's very common in modern house to have your basic bass have at least a sub, a mid crunch and then a side crunch layer. On top of that he also does a ton of fattening and compression in post. 

Now, the sound itself is very good and can actually be used in multiple of his tracks but there is no way to save all of the layers and post-processing...unless with patchers. So, you don't even need to have made the patches initially in Patcher but once you are satisfied you can drag everything in patcher and have all of it saved as a nice patcher preset that you can drag in fully ready.

*Intermezzo: from the FL manual it seems that you can even drag modulation macro stuff in it and that even the mod stuff can be routed to only certain routes.*

Of course, sometimes you may want to save presets but without post-processing or layers so regular presets without patcher are ok too. Or maybe you want to save the presets but without certain FX so you can make a seperate patcher again with only the FX (and layers) you want as a preset.

### Parallel processing
It's very common to EQ your delays and your reverbs without the EQ affecting our original sounds. For this you'd need multiple send mixer tracks. In patcher, however, all you need to do is simply have two paths, one with your dry signal and then the other with your reverb (again want to have 100% wet on these fx) and then afterwards an EQ and then at the end you let them both go to the output. Easy!

Now, I don't kow about PP when multiple instruments need the same PP how to reuse the patcher (I guess multipe patcher presets or better way?) but yeah it's cool.

There are also other parallel processing ways. Like maybe you want your sound to be crunchy and distorted but you don't want to run it through the reverb so again you make multiple paths and stuff.

### Visualizing
Doing stuff in patcher may also just help visualize your signal flow better, certainly if you have multiple parallel routing/processing going on. So for the visual learners it's just something cool.

## Setting up a template
Setting up a template is the same as making a project file. Of course in a template project rather than composing a song you may add some preprogrammed automation, synth racks, coloring if you're into that, send tracks and stuff like that. Add anything that'll make your life easier.

The template needs to be saved in a location similar to D:\Program Files\Image-Line\FL Studio 20\Data\Templates (So depends on your drive). Also, in settings you can change the default template to yourq id you want to use it for most projects anyway.

One note, saving it in the templates folder will make it be recognized as a template so anything you then do in the template is seen as a project and you can save it as is. If you want to edit the template file, instead of starting a "File > new" project you'll need to directly open the template file itself and then safe stuff to it.

Sources:
- https://www.youtube.com/watch?v=N11la5x5MDk&
- https://www.youtube.com/watch?v=AMCm6qtYkh8 (See patcher trick chapter)
- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Patcher.htm
