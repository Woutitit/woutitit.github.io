# How to mix and master
## Introduction
Unlike popular belief, mastering is mostly about enhancing and coloring the mix the way you want it. This can mean adding a tiny dot of reverb, adding some extra width, perhaps reshaping your mix's EQ curve a bit and stuff like that.

## Relevant resources
- https://www.youtube.com/watch?v=_2XIICPAYpk
- https://www.youtube.com/watch?v=ypy8_rHLG30

## Use Ozone 9
Ozone 9 is an all-in-one mastering chain (even though it takes up only one slot in FL studio, handy), as is Maximus to a lesser extend (it also has stereo stuff and saturation). It has an assistant and all the plugins you can place in there to master.

## Mastering basic chain order
- https://www.youtube.com/watch?v=_2XIICPAYpk

- Dynamics (compression/MB for peak reducing)
- Equalizing
- Stereo imaging
- Limiting

What is a maximizer then?

## To master for loudness or not
> Maybe put this point in the production tips article. 

Tl;DR: Kind of.

The loudness wars have been raging for a few years now. What it means is that people simply compress and push the gain as much as they can so they can get the absolute most out of the loudness of the song before it starts to distort. Basically, you want to put a limiter at 0db and be able to push the gain up as much as you can and the one that can do it the most (without distorting) wins the loudness wars. 

The reason people did this is because loud songs sounds better in human ears especially if you hear a quiet song and then afterwards a loud song. This was done in ads for tv where advertisers tried to be louder than the one before them just to catch the listeners attention more.

These days, though, we have loudness normalization on streaming services that basically have very intelligent ways to look at the actual loudness of a song and then balance all songs to be of similar actual loudness on the service. One of those ways is LUFS (developed in light of the advertisers trying to push loudness on tv). Basically, if you have a song with a lot of transients and then the same song super compressed just for loudness sake, both will kind of be normalized to sound the same volume on the streaming services because the LUFS doesn't look at peaks but more like a very intelligent average loudness, which for both songs are kind of the same (like it's the sausage in the middle of transients/peaks on a visual audio file). However, the one song still has all its punch and transients while the other has that all compressed out of the song.

This is why the loudness wars are over in that regard. You do not need to pull exagerated mastering and compression techniques (that don't bring anything to the quality or fatness of the song but loudness) only so that your song is louder than the others on Spotify.

To illustrate all this, look at the image here: https://hyperbitsmusic.com/ultimate-guide-to-the-loudness-war/. If a track is not compressed vs. overly compressed on a normalized service, you'll have a track that in some areas is simply louder than the compressed track. This is a really good development for songs that take advantage of dynamic range such as more traditional songs like classical, jazz and film music since now they can actually have loud sections in the song.

That said, the left track is less consistent in it's dynamic range which thus results in louder parts and quieter parts both on a micro and macro scale. This is not what we particularly want in modern EDM and pop music since we want consistency and fatness all across the whole song. So, those kind of tracks will still be heavily compressed and stuff to be fat and consistent (basically still look like a sausage more or less). BUT, the difference is, though, that most of the time our drums are the the louder transients that we want to have punchy but that often sounded flat due to the overcompression for loudness. So, while we have our sausage, we can still leave a bit of range for our drums to actually breath and bring in the propery punch we want and that is one of the main advantages for modern EDM and commercial stuff. Maybe this holds true for other transients you may want to retain a bit more.

One caveat, though, not every device and service has loudness normalization so not mastering for loudness would mean that on those services and devices you may potentially have a quiet song. Also, you can turn off loudness normalzaition in Spotify.

Either way, to summarize, for EDM and modern stuff, you still want to **master AND mix and compress and MB and OTT and saturate for fatness** but you don't necessarily need to compress with the sole function to destroy your tracks simply to gain a few dbs in loudness but at a price of completely sucking the life out of your track and/or audibly disorting it. Rather, try to find the sweet spot between getting stuff to be loud and fat but also still (perceivably) punchy. So, most loudness advice still applies but don't destroy your tracks over it.

## To mix for loudness or not
> Put this in the mixing and mastering article.

So theoretically you wouldn't really need a whole lot on the master to make your mix sound loud and fat. You can get 80% there by doing it in the mix if you need it. Now I'm mainly talking EDM and modern stuff where we like to have a lot of fatness and loudness. Simply compressing the shit out of stuff, distorting stuff, clipping stuff can all be done on individual elements already so you don't need to rely (that heavily) on the master to solve this, it can all happen in the mix itself.

That said, of course it depends. For EDM you want to multi-band, compress, distort the shit out of a lot of stuff but again it depends on genre and the instruments.

## To leave headroom or not
- https://medium.com/@adrian.price/common-music-production-myths-bb7c4880aaa0
- https://theproaudiofiles.com/6-db-headroom-mastering-myth-explained/

TL;DR: Nope.

Mastering engineers back in the old days asked for "-6db headroom", that is 6db until stuff starts to clip. Reason being that if you're song is at 0db, there isn't much for mastering engineers that they can do in terms of balance reshaping, coloring, adding loudness without stuff clipping and apparently turning down the volume of the track wasn't an option as it screwed up the quality or balances or something.

Either way, the point is, in our current *digital* age it doesn't matter at all since all a master engineer needs to do is pull down -6db on the pre-master (i.e. the audio file of the mix before mastering) if he wants the 6db of headroom. Pulling it down comes without any cost.

## Preparing the pre-master
### Avoid clipping
Make sure your pre-master doesn't clip so that when rendered out to go to mastering there aren't bad sounding artifacts in it. Since it's rendered out, there is no way to fix those at the mastering stage. Also, if you want to soft clip the master to color the mix, you can do that in mastering stage and simply keep your pre-master clean. It's way more flexible since you can tweak the order in the fx chain, severeness and shape of the clipping based on all the other master fx you have.

*Intermezzo: If your pre-master is close to hitting 0db at some points you may want to turn it a bit down if you want to be cautious and assure yourself that your pre-master isn't clipping. Again, as said in one of the previous tips, whether your pre-master is at -20db or 0db doesn't matter since you can just turn it up/down with the volume fader, so rather be more cautious than potentially too hot.*

### Don't brickwall
With headroom not mattering, there is even less reason to brickwall your pre-master. Again, some pre-masters are naturally more compressed and brickwalled (like EDM) than others (traditional jazz) but leave in all the natural dynamics and transients that are (still) there because once you compressed them out of your track, you cannot get them back. Therefore, just leave those things in so that in the mastering stage you can make the decisions on how much of those dynamics you leave in and/or how (much) you process/compress/limit the dynamics.

### Little dynamic range
Modern mixes naturally have very little dynamic range because the consistency is nice for the listener since the listener doesn't need to turn up and/or turn down your song all the time. And also, the loudness and consistency is what we perceive as "better" and "bigger" and whatever than something less compressed and more dynamic.

*Intermezzo: In quieter sections, usually other techniques are used other than taking away volume (like having low-passes, plucks at high volume) so that even at those point the volume is close to the peak loudness in the song. Of course, there might be some (brief) moments where the music is considerably less loud but it's usually and perhaps the perceived loudness (high frequency content) is still there.*

At the end of the master chain (?) we usually have a brickwall limiter to first of all make sure there are no potential sounds that are too loud but also to make our dynamic range even more flattened out, consistent and loud (in terms of gain but also RMS/LUFS). The problem is though, that when too much sections have too much difference in dynamic range, there is no good setting for the brickwall limiter. If the verse is super quiet compared to the chorus, then you'll need to push up the gain more so that the verse (at the very least the peaks) hit the 0db mark but then you may be distorting the chorus.

In this case, you either live with certain too quiet sections (which don't sound consistent, big and better to the public) or too distorted sections which isn't better. A better solution is to fix it in the mix whether that means more compression in certain elements, compositional stuff, volume rebalancing, whatever it is to make all the sections be more consistent in loudness.

*Intermezzo: A **good trick** is to occasionally render out a mastered (or unmastered) version of your track and check the dynamics. Your track needs to look more or less like a sausage. Of course, depending on the section and busyness the sausage may be a bit more fatter in some parts than others. Every part that doesn't come quiet to the tops of the dynamic range you have to investigage. For example, if your verse is a couple of dbs less loud than your chorus then you'll actually probably want to turn up your verse by either adding maybe some transient plucks to reach the loudness or turning your stuff up that you already have or adding other stuff to come there (or semi-fix it by pulling your brickwall limiter a bit more down but you may find it distorts the rest too much or loses too much punch). Else, your verse will just sound weak and your chorus will sound super loud. Now, mind that not every section and little part needs to come at the top. For example, you don't have to artificially try to raise a (very) quiet part to reach the absolute. And it's also not necessary. However, the most parts of your song should be reaching it (assuming a modern pop-ish production).*

Lastly, a few notes. First of all, this advice is for my own personal modern mixes that are leaning toward commercial stuff or EDM stuff. For more traditional music, there is no need for most of your song to be hitting 0db since playing with dynamics may be part of the song. Same with certain sections in EDM, while most part of your song should be more or less a sausage (read: equal in volume/peak loudness) there may always be "super quidet" parts that simply aren't meant to hit 0db and that's okay. You just need to recognize when that's okay and when you'd need to rework the section to be more loud (as of course, while it may not need to hit 0db it shouldn't also be too too quiet).

few things avoids clipping tho some use it to taste but u'd want to use soft and not hard clipping

## EQ balancing
Usually you'll do some (minor) frequency balance. Common things are a -1db on lows and +1 on highs or you may want to match your reference a bit more. Either way, it should be subtle and if you find yourself doing too much you might want to fix it in the mix for a cleaner result.

Dent in around 2k frequency range because that's very common where ears are super painful.

## Stereo imaging
You'll usually stereo image the bands. The sub you'll put in mono, the mids you'll give some width and for the air and hugeness you usually give the highs a lot of width (I think?) as a general guideline.

Also, often shelving the mids in the high frequencies a bit to then boost the sides in the high frequencies so you can push+hear/boost(?) the lows and mids (which are usually mono/more mono) in the mid signal.

## Brickwall limiter
At the end(?) of a mastering chain comes the brickwall. This is basically a limiter (what ADSR settings though) where you can do two things. Either you push it down until you hit your loudest points in the loudest parts of the mix (a bit further) and then you're sure that nothing above that is sounding. Or, in heavy/modern genres, you might push this even more down up until the point where you lose punch and/or where it starts to distort. This is for the even louder in your face vibe but if the music doesn't call for it, just brickwall it as good practice since there may always be some very short high transients that you'll want to chop off (especially with LUFS you might not need super brickwal). Though keep a true peak meter in your shelf to check as well some stuff.

Also, a little tip. Rather than bringing down the ceiling of the limiter to brickwall your mix, you should have your ceiling at 0db, the point where the audio would clip (why clip though?) and then push your mix, with the gain knob in the limiter, to the 0db ceiling (in Fruity Limiter). Depending on whether you want your mix's dynamics to be fully out of there (think modern EDM) or still keep them (think a more traditional orchestra or jazz song) you can either push your gain up until it distorts too much (for the modern edm) or at least until a few peaks reach 0db (else you're just missing out on free loudness) in case of the more traditional song.
