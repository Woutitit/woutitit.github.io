# Loudness normalization (LUFS/RMS/Peak/Mastering)
## Sources
https://www.tcelectronic.com/loudness-explained.html
https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/mixer_levelsandmixing.htm#loudnesswars
https://www.masteringthemix.com/blogs/learn/mixing-and-mastering-using-lufs
https://old.reddit.com/r/mixingmastering/comments/lt1ptl/progressing_my_mixes_and_i_feel_like_something_is/gounsuc/

## Table of contents
1. Loudness normalization
2. How to measure loudness and LUFS
3. What it means for mixing and mastering
4. Conclusion
5. Notes

## Loudness normalization
These days a lot of streaming platforms use loudness normalization (https://artists.spotify.com/faq/mastering-and-loudness) whenever they playback tracks. What this means is that they are going to turn up or turn down your track depending on how loud it is in an effort to normalize all tracks being equally loud.

**Intermezzo: We'll talk later about the way to measure loudness but note that streaming services don't do it with LUFS (see later) but LUFS seemingly come very close so it's still kind of relevant for us in terms of referencing and monitoring.**

### Why normalization
So why do streaming services do that? Well, it's because every song gets mastered at a difference loudness. One track will sound way louder than another track and another track might sound quieter than one track. As a listener this inconsistency is annoying because it means you might need to up or downscale your volume depending on a track by track basis. Instead, with normalization there is (or tries to be) a smooth listening experience where every track you're listening to sounds about the same in loudness (volume) which our ears and our volume knob likes.

**Intermezzo: Normalization comes from broadcast tv where they wanted advertisements to be all equal loudness so you didn't need to constantely turn up or turn down the tv or have some advertisements blast your ears off.**

Another reason is that it has been cited that louder (in volume) music sounds better than quiet music. This is why people turned up the gain on their songs to be as loud possible. Now, since audio starts to clip at at 0db (see "Compression > Clipping" article) people that had songs with a considerable amount of dynamic range started compressing the hell out of their music just so they could push the gain knob even further without clipping in an effort to make their songs louder than the competition (loudness wars!). Of course, to the detriment of punch, dynamic excitement, audio quality and the likes that gets lost by doing stuff like heavy compression. Thanks to the normalization this is (partially?) not necessary anymore since tracks now all get normalized to be the same loudness. This is a good thing because it allows tracks and genres that really weren't meant to be over compressed to breath and get their dynamics back without losing loudness.

## How to measure loudness and LUFS
https://www.youtube.com/watch?v=vidK3mE5Mn0&t=181s

Now, of course, making tracks equally loud is hard to do because how do you really make a noticeably dynamic jazzy song as loudly perceived as a super compressed fat dubstep song. 

**Note: In all these cases you should probably compare the fullest part of two songs with eachother to measure and compare loudness as less full parts can be a bit less loud.**

The first technique was to look at the sample-peaks (different than true peaks, see later). If the peaks were equal, then they were loudness matched. Of course, this is a very bad way of doing because below the highest peak of the dubstep track is all this fatness and sound while with the jazz track below the highest peak we gotta go a bit down before we see the meat of the track.

That's where RMS comes in. Basically this is the average loudness of your track. It factors in peaks but also factors in the main body of your track, i.e. the average of all these little peaks in your song is the RMS of your song. Level matching tracks in terms of RMS could lead you to some form of equal loudness because the dubstep song would now be turned down way below to match the RMS of the jazz song since its RMS lies way lower (since it has big peaks which could potentially drive up the average, but since they are most likely very short transients so they don't add to the RMS of the jazz song). Again, the dubstep song might still sound a bit louder overall but that also has to do a bit with how busy and fat these tracks are in comparison to a jazz track.

Now, the actual modern way is to actually use LUFS as that is currently the best way to really measure loudness. The problem is that RMS is just a flat measure of the signal. This means a boomy big low-end can really skew the RMS. However, since we perceive low-end as not that loud, even if we see our RMS is high, we might not hear it as high as a song that gets its RMS pushed mainly by high-end (which we perceive as louder naturally). Therefore, you can see LUFS kind of as weighted, more sophisticated, EQed, accomodated to our ears RMS. It takes into account perceived loudness (and other things) and now if you try to LUFS match the dubstep track compared to the jazz track, they will lie even closer as in how loud they both sound. Again, LUFS is also not perfect and again, a dubstep track is super fat so the dubstep track might always be as louder (which is more likely fatter most of the time, not louder in DBs) no matter what.

**Intermezzo 1: There is LKFS(what is this? does it matter?), LU and LUFS. LUFS is compared to 0dbs which is why the LUFS number is always negative LU is compared to the loudest peak of your song. You also have intefrated LUFS, etc., what do these matter?.**

**Intermezzo 2: LUFS is matched with db. If a song hits -5 LUFS and the other hits -15 LUFS all you have to do is literally turn down or your master gain control with the difference in LUFS. In this case 10db either up or down, thus very easy to LUFS match songs and thus compare the loudness and fatness (or hit a certain LUFS target for some reason, e.g. to simulate how it would sound on a certain streaming platform).**

**Intermezzo 3: You don't need to target -14 LUFS for example for Spotify. That defeats the purpose of the normalisation that does it for you.**

## What it means for mastering
In essence, whether your track hits -20 LUFS or -5 LUFS does not really matter since streaming services will either turn that down or up anyway. What could matter is the dynamics in your song. Say that your track is hitting -4 LUFS (which is pretty loud). The streaming services will turn it down to -14 LUFS anyway. Your track might sound fine but this 10db of margin is basically an opportunity to go check and listen to your track and see if there are points where you can be less thight on the compression and essentially open up the dynamic range more to allow some punch and dynamic excitement back in. Basically try to be less thight on all the loudness mixing things you did and see if you like the added back dynamics and then compare both at -14 LUFS and see which you like more. Again, at this point it's basically checking whether you like the slightly less fat but more punchy dynamic master more than the more fat one. They'll both playback just as loud.

**Intermezzo: When doing these changes always compare/check the loudest/busiest part of the track (and check LUFS there) since that's where the loudness compression obviously happens and thus where the changes will make a difference. Other parts might be useful for referencing though**

### Are the loudness wars over?
So with this normalisation, you'd think there is no real reason to participate in loudness wars, right? Well, yes and no. The loudness wars were detrimental because people would overcompress their tracks just for the sake of loudness. The compression for taming and making slightly more fatter wasn't enough, people would compress a ton just to squeeze out those extra dbs to push the gain knob. In terms of this, the loudness wars is over as overcompression is basically just a loss in quality and punch and it doesn't matter anymore.

That said though, as the reddit comment says, for that poppy, electronic genre "in your face" sound, compression really is the way to go. And on top of that, having very little dynamic range (so a lot of compression) is very essential for mainstream club bangers, radio songs, EDM, electronic stuff, etc as you desire consistency (and fatness) so your song can be heard throughout at the same volume. You want a steady beat and a steady groove all the way through even on the more "quieter/softer" sections. This is where it becomes important to properly compress stuff and basically apply loudness techniques just to squash the dynamic range as much as possible without losing too much punch or other stuff. Properly composing and arranging also helps (like turn up piano in quieter sections so the dynamics don't change too much, or add some percs or whatever to keep the perceived loudness going without having to do a mega-squash).

So yeah, for that modern "in your face" sound, you'll still want to compress a shitton and brickwall your master and stuff. The only thing that changes is, again, when you like (the fatness of) your mix you don't need to overcompress or compress even harder to squeeze those last dbs out. Don't do it, keep some punch and your mix audio quality will be better and more alive sounding. 

Also, your audio won't always be normalized (?), like certain speakers, etc. So there it still pays off if you have a song that is naturally very loud. (Trade off, or make multiple masters then?)

As said, compression and other loudness techniques do make sound fatter. So especially in stuff like EDM and dubstep and electronic (and even pop) you're pretty much compressing (the shit out of stuff) for the sake of making individual tracks (much) fat. On the master you're then compressing kinda hard too (also put OTT) just to make everything even more fat and aggressive and in your face sounding.

Of course, for stuff like jazz and orchestra or stuff that you don't want super in your face, there is no need for fatness compression. You can leave it dynamic if you like your mix like that with again the added benefit that you do not need to overcompress just to make your track louder sounding.

### So, what to do?
https://www.reddit.com/r/edmproduction/comments/8t8dki/how_are_dubstep_producers_able_to_get_a_3_luf/e15l5l4?utm_source=share&utm_medium=web2x&context=3
https://www.reddit.com/r/edmproduction/comments/9kcr9c/the_loudness_war/e6yrrsm?utm_source=share&utm_medium=web2x&context=3

In general, limit your master and compress your tracks as much as it needs. If it s a club banger, pop songy, go for in your face little dynamic range whilst trying to preserve some dynamics and punch. If you're going for sem-jazz, try to preserve some dynamics but still try to push it as much. If going for real jazz and or orchestral, go for preserving dynamics but again try to push it with the limiter and compressor and EQ (to be able to raise volume) or saturator as much as you can without compromising too much. By default, push as much as you can the limiter. How much depends on genre, track, etc. Just load in some of you favorite tracks and see how much or little they pushed the enveloppe.

So yeah, again, it depends on the genre what you want to do with it. Jazz and orchestra is very dynamic in nature, pop and dubstep isn't at all.  You probably don't want jazz and orchestral to be too out of wack dynamics wise so you'll put some measures in place in terms of dynamics management but you can decide how much. Same with aggressive in your face fat pop or dubstep which might initially be too dynamic and flat and unpunchy (even with techniques to keep punch, perceived dynamics etc.) you might want to dial it back. It's basically a spectrum of dynamics and for each genre and each song the answer of loudness vs. dynamics will lay somewhere in the middle with either a left or right bias based on that genre or song.

**Intermezzo: Checkout the LUFS on your favorite tracks. For example, a lot of hard hitting dubstep will playback at -14 LUFS, on spotify just like your own dubstep track but pull it in your DAW and you'll see it hits at 3-4 LUFS. This is very loud and requires a shitton of compression to be able to reach without distortion. Some of these tracks might have indeed been pushed too hard the sake of loudness but even at 5-6 LUFS it's still a loudness that can only be achieved through compression, proper mixing, properly fattening up sounds and layering and stuff. In other words, if you level match your dubstep track to the dubstep one and yours sounds unnaggresive and thin, it's probably because your fatness and compression is not that good that you can't turn it up all the way up to 5-6 LUFS without distorting. But again, dubstep is extreme but for most modern you do want a certain fatness and compressionnes sound regardless.**

## Conclusion
In conclusion, you want to still strive to make your music sound as fat and consistent (litlle dynamic range) as possible (since louder/fatter still sounds better) keeping in mind the genre. That might mean not very fat and quite inconsistent (real jazz and orchestra) or very fat and rather consistent (dubstep) but it's a spectrum. 

The change that happens with the normalization is that there is no need to start OVERLY compressing and limiting your tracks and masters just for the sake of the extra couple of dbs in gain loudness but no real gains at fatness (like the extra fatness is worse than the loss in punch) at the expensive of punch and dynamic excitement. Figure out what you want, compare to reference tracks (LUFS) but for most rather commercial stuff, club stuff, and electronic stuff you do usually will be at the side of more compressed and consistent than the other side.

## Notes
crest factor? crest factor vs dynamic range?

true peak? like its a peak barely audible between samples, does it matter? do i have to put on true peak limiter on master?
or do i not care?
starts in composition
This is where you basically have 10db of headroom to take a look at your track and check whether you can lose some compression here and

true peak bad cuz lossy formats might which is why u want ur peak to be max -1db or whatever or 0.1db or whatever?


Like u got compression for sustain or more transient or fatness or u got compression for loudness sake. Sometimes overlap.

spotify and shit use other shit than lufs but similar to lufs so some kind ametric

also 6db headroom if knbow services gonna turn it odwn

 This a much better way to loudness match tracks

compare against loudest part of ur song thats where u wanna base ur lufs etc. on

also loud tracks are produced with loudness in mind so even in quiet sections try to have stuff that is loud kinda (like a quiet velocity wise piano but turned up involume or some percs or whatever)


in fl orange means its almost clipping, red means it IS clipping in fl also all the faders are -6db so u got headroom by ddefault anyway

 This meant that people started pushing their tracks to be as loud as possible (and preferably louder than anyone else).



but the no dynamic is also a really consistent in ur face sound that clubby and electronic genres rely on so its not all bad (?)

 Playback the same version of a track with one being quieter than the other (but not too much) and people will prefer the louder track. Therefore, in order to avoid people gaming the system and using all tricks in the book



 (such as heavy compression to allow turning up the gain as much as possible until the peaks reach 0db close as possible to 0db without clipping) turning the gain all the way up to be louder (and thus better) than others, norm

how to meter loudness?



couldnt push a jazz track as high like just with the gain simply right? Or then it starts to distort cuz 0db???

This is normal text.

Paragraphs are separated with two newlines.

1. This is an ordered list.
2. There are two items on this list.

- This is an unordered list.
- There are also two items on this list.

```
This is a code block
with multiple lines
```

Supported markdown syntax can be found on the guide bar.

LUFS is better at actually perceivin g loudness cuz its more based on our hear like there is wieghted shit in there like more attenuated to high-end. Like ur RMS of another track could be the same but it might be because of ur bass which is booming and actuallyu out of control compared to high end. LUFS will highlight that as you'll have less LUFS

so why still important to master for loudness or only master for reducing dynamic range then or?

also point of loudness potential and now we talking thicness fatness vs dynamics and not perceived volume

want seperate master for clubs since they dont have normalization and look at peak so ud wanna compress more to be heard
and make sure ur song doesnt get turned down in volume just cuz there is one huge peak in ur song. Or is that the same master
like what if the speaker plays from spotify does it matter?

Do i need to target minus 14 LUFS though?

dynamic processing detrimental to sound so if u come in hot at +6DB there is room of 6db to make ur song more dynamic again and potentially allow more punch and stuff

