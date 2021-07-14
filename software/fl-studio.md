# FL Studio
Todo: Maybe make a seperate article for all or some FL Studio native plugins?

## Resources
- Automation clips basics: https://www.youtube.com/watch?v=cK8uiEngm5g

## Transient processor
- https://www.image-line.com/fl-studio/plugins/transient-processor
- https://www.youtube.com/watch?v=3QpZYSUljmw&t=211s

So transient processor is kind of like a magic compressor though the attack doesn't have anything to do with how fast it kicks in and release also doesn't have to do with how fast it let's go. The attack simply magically kind of looks at the beginning attack/transient part of a sound and then you can spin the dial and literally just make that part louder or quieter so either making it less or more punchy. With the release knob, it looks more at the body/end of a sound and again you literally can pull it more up or put it more down depending on what you want or need. So yeah a bit like a saturator/compressor does. Not sure if saturation makes it even more fatter than just processing but with this you get a lot of control on how punchy and/or fat you want your stuff to sound like.

It seems that saturation still makes stuff fatter (if needed) but that you may be able to do TP before or after to add some more transient back in or even more punch in if needed but that you still want clipping/saturation for fatness (?).

Also, it even works on a synth INIT patch (so full sustain no attack no release) and it will give it some attack (I guess so in that case or all cases it looks at a certain amount in ms in the beginning and shapes that), however, the release didn't work because the stuff is flat and not dynamic at all and also the attack was also just a little thump and stuff. So again, transient shaper works best on synth patches, instruments (such as percussion and plucks) that have transients/dynamics/fading tail and thus are meant to be more stabb/percussive. So it's for transient-functional sounds to be enhanced and shaped even more in their transients.

## Playing MIDI
Well, the easiest way is to File > Import and then just leave everything. It will load in all MIDI and with Flex instruments and that's good as Flex has instruments that follow the standard MIDI things so it will fill in everything nicely. On top, you can easily modify MIDI, change instruments or even mix so very handy!

## Styleguide
### Colors
Bus = #000

## Color coding and renaming
- https://www.youtube.com/watch?v=JaHj3BS61oc&t=193s

So it seems a bit clunky still. What I'd do is have a styleguide (see here) sheet with "Bass = x color" (in HEX) and "Lead = y color" and "Buss = z color" and so on for consistency and easy choosing accross projects. Don't worry about edge cases just have the basics in there (like bass, lead, buss...). Like a styleguide perhaps it can be called. Same thing for color coding, you don't need to color code everything because you'll get a headache, just do ones that are obvious (such as busses) and lead layers and bass layers and stuff like that.

But basically what you want to do is simply, if it's channel rack, vertical drag accross all the green rectangels you all want the same color. And then click arrow left top on channel rack and then "Color selected". Give it a gradient but with left and right color the same so all colors are the same. And boom all your stuff is now colored. Now, the stupid thing is that you need to do that in the mixer now again too. In that case it's ctrl + horizontal drag over the mixer channels and then F2 and then give it that same color you just gave. Playlist is irrelevant as I do everything in a single pattern.

But yeah it's a bit stupid so in the future I could have colors setup but even then it may not be a big timesaver.

## Add layer
> There may be a shortcut to add layer

Basically you can add Layer as a VST just like Sytrus or Serum. And then you need to copy the MIDI in the layer and then you need to select all VSTS that need to use that layer in the channel rack with the small vertical rectangle that turns green and then in layer hit the option "Set children" and you're done.

## Patcher
- https://www.youtube.com/watch?v=N11la5x5MDk&
- https://www.youtube.com/watch?v=AMCm6qtYkh8 (See patcher trick chapter)
- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Patcher.htm

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

## Volume automation sidechaining
- https://www.youtube.com/watch?v=9LyciXjMD-U

Usually you have one (or more depending on whether you need different slopes for different instruments) or more SC inserts and everything that needs to have sidechaining you disconnect the direct routing to the master and instead feed it to the SC insert to your liking (and then the SC goes to master).

A basic volume automation SC starting point is a beat long and has two points, one half way the beat and one at the end of the beat. The half way one is usually at full volume (0.8 in value) so from there it's horizontally to the end and from the start to the half is a straight linear line. This is a good starting point but the slope will depend on kick and/or effect you want. Also the half way point does not need to be at full volume already, you may want to lower it a bit and have a bit of a slope until the end. Again depends on your kick and/or effect you want. Finally, for the automation, don't use the fader but use "Fruity Balance" for more flexibility.

Protip: Make a sidechain automation preset under "Channel presets" and/or even make a template with a SC route already ready. Something like Synthion who has a SC lane and already 1 bar (4 beat) of 4 SC automations). See: https://www.youtube.com/watch?v=MDkJckTswJQ.

## Automation clip shortening
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls

It seems right now, it's a bit of a drag to organize automation clips since you cannot truly shorten them. Therefore, if you don't need the automation clip running for the whole song, for your own sake, you are best to just hightlight a small portion and then make the clip as big as you need it it to be. Easier reuse and you can actually merge short clips together like that.

## Shortcuts
> If you hover over certain tools it may give you a shortcut option.

- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/basics_shortcuts.htm
- [comprehensive_compilation_of_advanced_fl_studio shortcuts](https://old.reddit.com/r/FL_Studio/comments/ep7jlf/comprehensive_compilation_of_advanced_fl_studio/)
- https://www.youtube.com/watch?v=RBw-pdqus3k&t=88s

### Mixer
- Ctrl + drag = select multiple tracks

### Playlist
- Shift + P = select draw
- Shift + B = select brush
- Shift + C = select cut
- Shift (in playlist) = cutting
- Ctrl + T in playlist = timestamp
- Ctrl + G when selecting multiple patterns = merging (works both vertically and horizontally)
- Ctrl + Alt + G Same as above but for automation clips
- Alt + Dragging (?) on velocity = normalizing notes on default velocity
- Ctrl + Drag = Keep vertically aligned whilst dragging
- Shift + Drag = Keep horizontally aligned whilst dragging
- Shift + Cut = Keep straight while cutting

## Troubleshoot
### 3rd-party VSTs loses focus after knob tweak
On top of your VST (on the Fruity Wrapper top bar) you'll see to the right (somewhere next to the 'x' icon) a keyboard thingy. You have to toggle that (see below picture, though, on the picture you can't see it well as it's half out of frame):

![nklz651m1x461](https://user-images.githubusercontent.com/17428965/113638649-a648de00-9677-11eb-8427-04c95c4888af.png)

### I forgot to record my MIDI keyboard
Go to Tools > dump latest recorded score to recover what you've played in a pattern.

### Controls (like fader) jump to different value when pressing play
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls
If you ever initialized a control with an automation clip, the state is now saved in FL so even when the automation clip isn't there, the initial state of what you had will be the state your sound will jump to (like the volume fader or whatever).
