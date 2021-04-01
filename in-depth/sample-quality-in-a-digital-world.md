## Audio quality & Recording

## Table of content
1. A bit of history
2. Analog vs. Digital recording
3. DAC/ADCS & Storing sound digitally
4. AD/DA Conversion
5. AD Conversion: Sampling
6. Sample rate & Audio Quality
7. THEORETICAL Reconstruction Accuracy: A theorem & a formula
8. Nyquist-Shannon theorem: a closer look
9. Low sample rate, aliasing & uniqueness
10. Bandlimiting
11. PRACTICAL Reconstruction Accuracy: Quantization
12. Bit depth
13. Quantization noise
14. Low bit depth and dither
15. Signal-to-noise ratio (SNR)
17. Conclusion
18. FAQ
19. General sources
20. TODOs
21. Unprocessed notes

## A bit of history
So all the way back in the 19th century there was no way to capture audio. Whatever was heard was forever gone and only captured in memory. That was until in that same age Thomas Edison (yes, that guy) invented the phonographe. Basically a device that could capture the vibration of analog sound through its horn which then got etched into a metal layer around a cillinder (https://nl.wikipedia.org/wiki/Fonograaf). This, in turn, was the precursor to the grammophone (https://nl.wikipedia.org/wiki/Platenspeler) which was basically an improved version that etched stuff into a vynl plate instead. Even later came tape recording (https://en.wikipedia.org/wiki/Tape_recorder) that also used some analog magnetic wizardry to store recordings of whatever sound information it got and was even more improvement upon its predecessors!

## Analog vs. Digital recording
So why the little history lesson? Well, it's important to note that these devices were all analog recording and playback devices. Because, as we said, recording back in the day was LITERALLY engraving a sound source into a physical object. And, since audible audio is per definition always analog, being able to capture that exact audio in an analog way actually was and thus still is the best audio quality (at least in theory) since there is no innacurate conversion or manipulation of the waveform needed to be able to store and playback the sound.

This raises the question: why did we change to digital recording and audio storage? Because in practice analog is far from perfect and does has several issues. First, with analog storage and recording noise gets easily introduced and the more and more something gets re-recorded the more noise gets introduced up until the point that what you recorded is really bad in quality. Also, with computers and programming languages on the rise it would be nice to do some wacky algorithms on audio for fx (like you can only manipulate digital numbers, not analog things). Sadly though, analog is uninterpretetable by a computer so we can't write programs (like plugins) for it.

Now, these are just a few issues, there are more:
https://en.wikipedia.org/wiki/Comparison_of_analog_and_digital_recording#Main_differences
https://www.reddit.com/r/WeAreTheMusicMakers/comments/epfxs/for_those_who_think_analog_recording_is_better/
https://soundgirls.org/understanding-ad-da-converters/ (a bit down the article where it talks about signal processing and progammability)

The point is, digital is more reliable and is actually the only (easy) way to be able to work with and manipulate a sound in a digital world (because those sounds are stored as numbers, not an actual vibration). Also, we simply moved more and more to digital for everything and slowly but surely the craving for digital recording became too much that eventually it became a thing.

## DAC/ADC & Storing analog sound digitally
There is only one problem, digital is NOT analog and therefore we NEED some way to be able for the computer to interpret all this analog nonsense. This is where an audio interface with DAC/ADC comes in. What it does is basically convert an analog signal to a digital signal but also vice versa. So for example, if we want to record something, then the interface will CONVERT those vibrations to digital and whenever we want to playback something, the digital instructions for it will be converted by our interface to analog and will be send to our speakers/headphones/whatever.

Now, there is another problem. In the analog world, we could literally just capture and store continous things (such as sound) as they are (for reasons we already discussed). However, with digital recording and digital storage, there is no way for us to store (let alone do something with) an analog signal on a digital device. They are literally incompatible. Therefore, what we need to do is CONVERT this analog signal into digital numbers (which can then compile into machine code like 1's and 0's) that a computer can understand and store.

## AD/DA Conversion
Now, to convert an analog signal we must first understand that continuous data such as analog vibrations can't be stored on a digital medium. Analog data is not a number, an array of numbers or anything related to what a computer can understand and manipulate.

So how would we store we store an analog signal digitally then? Well, a computer works with numbers (that get compiled into binary) so in the case of a sound wave we could, in theory, chronologically store all of its amplitude values as discrete, unconnected numbers. And then, for playback purposes our DA converter would then simply take all these numbers and reconstruct the actual continuous analog wave out of those numbers.

But there is a problem. It would indeed be nice if we could store "all" the amplitude values of a continuous (=analog) sound wave because in that case conversion in both ways would be simple:

AD => Make our AD converter measure and store all analog continuous data as digital discrete data so that analog data = digital data
DA => Make our DA converter reconstruct a continous sound wave from the discrete data (We can do this with 100% accuracy since analog data = digital data) and send it our speakers.

The problem is, in the land of continuity, "all" means infinite. Therefore, unlike storing "all" continuous data in a continuous analog way, we actually can't store "all" continous data in a discrete digital way since that would require storing an infinite amount of numbers (so an infinite amount of storage space).

*SMALL INTERMEZZO: If the infinite thing doesn't make sense, think of how a digital camera captures IRL. IRL is continous but digital cameras these days only capture IRL at +60 FPS (That is 1 picture per 0.01667 second (said in another way, that is 60 pictures uniformly spread over 1 second). Therefore, when watching a 60 FPS video recording we're essentially "missing out" on all the stuff happening between the pictures. Of course, we can always take pictures per second even faster to "miss out" on even less per second but no matter how low you go, there is always a very, tiny amount of time between pictures where no pictures are taken and that we thus "miss out" on (this is the concept of continuous). Therefore, the only way to NOT miss out on ANYTHING IRL would be to literally have an INFINITE amount of pictures being captured per second to record the INFINITE amount of IRL happening in a second. Said otherwise, there is an infinte amount of time divisions you can make in a second and thus an infinite amount of pictures in a second you can take. And again, unless you're using analog recording techniques that is just literally impossible to do since we can't crank FPS to "infinite", like, infinite is not a number, it's a CONCEPT, how do you crank up to a concept? Next to that, even if we could record infinite the sheer amount of storage space it would take up would also be infinite.*

## AD Conversion: Sampling
So, if we can't store "all" the data, is there a way for us to still convert and store continuous analog data in a digital way? Well, yes there is and the solution is simple, instead of storing literally "all" the continuous data, we'll only measure (also called *sampling*) and store a part of it.

** INTERMEZZO: I can hear you think. If we don't store "all" the continuous data, how in the hell can that ever be accurate and representative of the analog waveform in any way? Well, I'm not going to thoroughly answer that just yet but know two things. First of all, human hearing (just like eye framerate) luckily has its limits. And we can exploit these limits to not have to store an INFINITE amount of sound wave data and still be able to preserve audio quality data (at least, to our ears). Also, if we were to write down our samples on a piece of paper we can actually mathematically derive the original soundwave from these samples with a 100% accuracy so we'll proof it's possible to preserve audio quality with a limited amount of samples. Non-mathematically speaking though, when you want to store these samples DIGITALLY and THEN reconstruct the soundwave from the stored numbers that it would indeed NOT be 100% accurate since we can't store sampled values on a computer without rounding/truncating them (as we'll see). Therefore, since we can't store the mathematically correct value and the samples are slightly rounded, the algorithm to reconstruct the soundwave will reconstruct a slightly different wave based on these slightly different rounded samples then what the original was (we'll explain why in a second, dont worry).**

Now, the concept of digital recording/sampling is simple. What we do is basically take uniformly spaced snapshots (called samples) of the currently recording analog wave. For every snapshot, we read the amplitude value of the analog wave at that point and then store that number on our digital device. After the recording is done, we then end up with a (finite) array of discrete amplitude values of the analog wave that we can now store and voila there we have our full AD conversion (I know I forgot one tiny detail but I'll come back to that later). 

(Later we'll see how to convert those numbers back to something actually continuous.)

## Sample rate & Audio Quality
Now of course, we can't just take random snapshots of the wave at random and expect our DA reconstruction algorithm to just reconstruct our orignal wave from that. No, we need to be aware of three conditions:
1) Sample at 1 steady rate (Hz) to make sampling predictable
2) Sample fast enough as to not lose audio quality
3) Sample little enough as to not have to store too much sample data

1) So this one is needed because as we'll see later for the sake of mathematical stuff, accuracy and reconstruction we need to have uniformly spaced reference points instead of random reference points. It just makes things predictable and mathematically easy to have all samples be equally spaced. And yes, we could theoretically even sample at a rate according to a repeating pattern (like x Hz for 2 seconds, y Hz for 3 seconds, x Hz for 2 seconds again, etc.) and still come to the same results as a steady pattern but then we're just making it mathematically incredibly hard for us (also, I'm not at all sure about this).

2) We need to sample at a high enough rate because the sample rate is what *partially* determines the quality of the waveform that you can later reconstruct. More specifically, the sample rate actually has an effect on **how accurate we can record frequencies** (we'll see in a bit what we mean with accuracy here). *If we sample at a high enough rate, we can actually later reconstruct the originally sampled wave with a 100% accuracy.*

3) There is a human upper limit to what we can hear in audio quality and frequency content. Therefore, it's not necessary to sample at a rate higher than what we can even hear in both frequency and audio quality since that will only eat up our storage space.

So, based on these points, for the sake of audio quality all we want to have is a *single, steady and high sample rate* that yields us enough samples to be able to later accurately reconvert these samples back into a continuous analog wave. Now, of course the question then arises: Is there any way to know what that sample rate should be exactly given ANY complex waveform? And also, what happens in the case that our sample rate is too low? Both of these questions can luckily be answered.

## THEORETICAL Reconstruction Accuracy: A theorem & a formula
So, there is a theorem out there called the *Nyquist-Shannon sampling theorem*. This theorem actually describes the MINIMUM sample rate at which we need to sample to be able to have enough amplitude values to reconstruct ANY original complex wave with 100% accuracy. If that minimum sample rate is not met, then we can still construct an output wave based on the samples we have but it will be inaccurate (so not REconstructed). 

Now, you might think, how do we even reconstruct a continous connected actual analog wave out of discrete unconnected values in the first place. What about all the stuff in between samples? Well, all of these values in between can actually be calculated through the *Whittaker-Shannon interpolation formula* (not sure if other formulas too). The only thing for this formula to be 100% accurate for any complex waveform at every sample timing is IF you have sampled enough samples, i.e. have a high enough sample rate (so when the condition that the NS theorem holds to accurately reproduce any sound wave is met).

** SMALL INTERMEZZO 1: Of course, the formula calculations are yet again infinite values but a DA converter can approximate these values through practical reconstruction techniques (interpolation such as zero-order hold + analog (?) filtering such as anti-image/smooth filtering). Don't worry about it too much here, though. Just assume that your DA follows the WhittakerÃ¢â‚¬â€œShannon interpolation formula in some magic way.**

** SMALL INTERMEZZO 2: The timing of when we sample a waveform does NOT matter. Look around 20:45 https://www.youtube.com/watch?v=cIQ9IXSUzuM here. The guy has artificially made it so that our sample points look like a square wave when graphed. However, besides the fact that digital samples are NOT connected, a square wave actually does NOT look like 2 horizontal lines where one's positive and the other negative. In reality, it has ripples and as we can see, even if our samples happened to look like a "perfect square wave" our formula can STILL calculate that there shouldn't be lines drawn between the points but actual curves to reconstruct the analog signal. He then also shows that you can shift the start of sample timing in any way and that the calculations will always keep adapting to keep reconstructing the exact same rippling square wave. Neat!**

## Nyquist-Shannon theorem: a closer look
Now, let's actually dive a bit deeper and see what the theorem is all about. Let's see what we mean with "accuracy" and let's also see what happens when we sample at a too low sample rate.

So, it turns out that there is actually a very simple and logical way to know at at which rate we need to sample for 100% accuracy. The thing is, all music is is basically a bunch of sine waves. A sine wave has both a positive and a negative stage. Well, it turns out that if we can *sample both the positive as well as the negative stage of EVERY cycle of EVERY sine wave AT LEAST ONCE each PER cycle* in our complex waveform that we then have enough samples to later reconstruct that complex waveform accurately. In other words, if we can CORRECTLY detect EVERY frequency of a complex waveform we can then later reconstruct that exact waveform through our Whittaker-Shannon interpolation formula.

And this is what we mean with sample rate and accuracy. Because, with a sample rate that is too low, it means that we cannot correctly identify and sample some frequencies accurately. What happens instead is that these inaccuracies will actually introduce something called aliasing.

But anyway, to see all of what we've talked about you really need to visualize it yourself. Draw a sine wave with 10 cycli and always pick one positive point and one negative point per cyclus. Then smoothly connect the dots. What you will notice is that you will end up with a sine wave that probably is different in amplitude (disregard that for now) BUT the same in frequency (it goes up and down when the real one does too and as fast as that one). In other words, with only two dots per cycle we are able to identify the frequency of that wave.

We cannot have, for any cycle, of any frequency only one sample for a positive stage but none for its corresponding negative stage or our samples won't be accurate enough to reconstruct from. You can try that. Take away some dots (even just ONE dot) in total and you'll see that you will now not be able to fully redraw the same frequency content as the original sound wave has. Therefore, we can conclude that *AT LEAST one pos/one neg dots are required per cyclus (you can try with more and you'll see you can construct the frequency image too).*

So, then the question rises: how do we guarantee for ANY complex waveform that we can record all of its frequency content accurately regardless of sample timing? Or else said, if all it takes to be accurate is to ALWAYS sample two points per cycle, at what sample rate can we GUARANTEE that we ALWAYS for EVERY cycle of EVERY frequency have AT LEAST one pos/one neg sample? Well, that's what the theorem states and it's apparently *at AT LEAST (or greater than) double the rate of what the highest frequency is of our recording* (this is called the *Nyquist rate*).

Now two questions:
1) Why at least double the rate?
2) Why double than the the highest frequency?

1) So, let's simplify for a second to see why we need at least double to be safe. Let's say we measure sound waves in meters. We have a 2 meter sound wave with both the negative and positive stage being equal in length of course, so 1 meter. According to the theorem our sample rate wave can be maximum 1 meter. Let's say that in our recording we happened to sample at 0.4m of the 2 meter. This one is clearly in the positive stage since we're not over 1 meter. Well, then our sample wave will have another sample at the end of one fully cycle which is at 0.4m + 1m = 1.4m and this one is clearly in the negative stage. We can go further even and say we happened to sample at 0.99m, barely positive. In that case we will have another sample at 0.99 + 1m = 1.99m, barely negative but negative nonetheless.  You see? No matter where we start sampling, even if it's at a barely positive amplitude value, having our sample rate be max equal in length to a stage makes sure that even at barely positive/negative samplings, our next sample will ALWAYS be somewhere in the next stage, it never skips a stage. With meter values less than 1 it's even better and we have even more breathing room (like 0.99m + 0.75m) =  1.74m. HOWEVER once we go over this 1m, like 1.02 meter, sampling the positive and negative stage can NOT be guaranteed. Like in this case, if we happened to sample at 0.99m then we would have 0.99m + 1.02m = 2.01 meter. So in this case our second sample would already be in the next cyclus, we skipped the negative stage. Now, in this minimal difference case, you'll still have a lot of one pos/one neg pair samples in one cyclus but as you can see it CAN'T be guaranteed for every sampling situation and cyclus and thus it can't be reliable.

**INTERMEZZO: One footnote here though is that if we had a sample rate of EXACTLY doube the highest frequency we want to sample, we can also not guarantee to have two samples per cyclus. Normally we should, but in the unlucky scenario where we happen to sample on the exact same point where the wave to be sampled is 0, all our samples will be 0 in amplitude too, and thus we won't have any frequency reconstructed. To say it with the meter example. If we sample at 0m with 1m, then we get 0 + 1 = 1m. However 1m is half of 2m and in a sound wave that point is 0 and thus we sample a 0. Then we sample again, so 1m + 1m = 2m but now we end up again at a point where the sampled wave is 0. And this cycle continous because 2 + 1m = 3m is right in half of the next part of wall (which starts at 2m and ends at 4m) etc. Therefore we always want to use AT LEAST MORE THAN double the sample rate of the frequency of the highest frequency.**

2) So why double than the highest frequency? Well, simple answer. The highest frequency is the fastest and thus requires the fastest sample rate to be able for us to take at least two samples per cycle. Therefore, if our sample rate is high enough for our absolute highest frequency we're recording, it's automatically high enough for anything below that too since those can have lower rates anyway to still have two points being recorded.

**INTERMEZZO: Now, obviously, we've only looked here at a simple sine wave. In a complex wave, the negative stages and positive stages might not follow equally to eachother and thus we might skip stages, right? Well, not really. You see, ultimately a complex wave consists of/can be reconstructed out of a whole bunch of added (?) sine waves - Fouriers series (what is Fourier transform?). Therefore, if we have a sample rate high enough to catch the highest frequency accurately of our recording (whether it'd be a harmonic or a fundamental tone) our complex wave will obviously be recorded accurately too since all the lower frequency sine waves within that complex waveform will also be recorded accurately at that sample rate. In other words, anytime we're recording, no matter how complex the sound wave, we don't need to take into account the full recording/frequency spectrum. Nope, we only need to take into account the highest frequency and see that we can record that one accurately. Also, in practice, what we'll do is simply sample at the highest rate a human can hear (44.1k, which has even a slight bugger) since it's very inconvenient to always have to check what the absolute maximum frequency is that we're currently recording and always have to adapt our sample rate. With that human limit we don't have to worry about it and it's still low enough that it doesn't take too much storage space anyway.**

## Low sample rate, aliasing & uniqueness
Now, what happens if our sample rate is too slow?
If our sample rate is too low and we captured too little snapshots, our DA converter simply does not have enough samples to be able to accurately reconstruct certain frequencies of the soundwave. Therefore, the resulting output will not be the same as the original input, resulting in reduced audio quality. Therefore, we thus want to be able to record just at a high enough sample rate that is able to record all the frequencies that a human can possibly hear with a 100% accuracy (so between 20-20k Hz) or else we can hear a loss in audio quality (depending on how slow the sample rate is, this can be easily audible or kind of hard). Recording anything above that sample rate can be done but is (usually) useless. Now, why exactly do too low sample rates affect the accuracy of our sampling? Well, to see this, you really need some visuals so I'd recommend watching/reading some sample rate stuff I've linked above. 

*TODO: // Explain aliasing and show how wave reconstruction is scuffed, don' here too. visuals**

Now, another thing to understand with this theorem is that if we don't meet the bandlimit requirement (or not have a high enough sample rate) we can actually end up with a set of sample points that might have originally come from our input signal wave but actually aren't unique to that wave. That is, from these discrete values we've sampled we could actually reconstruct other sound waves too other than just the original input sound wave (like we could draw some crazy wave curve bendings in between).

Now, in practice an interpolation algorithm isn't going to draw crazy wave bendings (since those also aren't real sound waves so impossible, look at blue drawing of FL studio video guy above link) in between samples. But, an interpolation algorithm obviously certainly has no way to tell what the original sound wave was from the set of values it gets. Therefore, the output signal we get is simply the result of smooth connection between all the discrete value points we had. Now, the problem here is that if we were to take a different input signal, that is different, but we were able at the same sample rate to take the exact same set of discrete values as we had for our first wave. Well in that case our interpolation is going to interpolate in the exact same way and thus render an exact same output waveform as for the first input signal.

So what can we tell from that? Well we can tell that for at least one input signal, whether it is the first or second, the output signal is wrong (or at least not 100% accurate). We can tell because for each unique input signal there can obviously only be one unique output signal that is 100% accurate (hint: it's the input signal of course). Now of course, it could very well be that the input signal of either the first or second wave is exactly what the output signal shows but than that output is obviously wrong for the other wave. Therefore we can conclude that in order for us to record any frequency accurately, the discrete values we take need to be unique to our input signal in order to reconstruct an output wave that is unique too and is thus a 100% accurate reconstruction of the input signal (so uniqueness = accuracy).

So, how do we ensure that? Well, again, that's what the nyquist theorem tells us. Remember what makes a wave unique is both its frequency and amplitude content. Between two waves that are different AT LEAST one frequency or amplitude value for frequency/sine wave will be different and thus, in the sampled values of the complex wave there will be at least one different sample value and thus a different wave that can be reconstructed.

More information about this can be found here:
- Around 5 min: https://www.youtube.com/watch?v=rsLD7dGlK-c 
- Around the end of the first chapter: https://www.youtube.com/watch?v=cIQ9IXSUzuM

So in conclusion, if the bandlimiting requirement is met, we will be able to sample AND reconstruct a sound wave with 100% accuracy. If the output signal would not be equal to the input, that automaticall means our interpolation did some rounding off of some signals which we couldn't capture accurately. And thus, these were signals beyond our band limit and thus ain't a correct solution anyway since in real life these will be actually rolled off (and thus that output signal won't happen in a real situation).

## Bandlimiting
Now, for our theorem to really hold up we do need to introduce one more concept: bandlimiting. Bandlimiting means that we're going to limit the maximum band/frequency that we're going to record. Therefore any frequencies that would have been beyond that band will be completely filtered out (at least in theory, in practice sometimes error here and there, therefore you need buffer as we'll see later).

We need a bandlimit because only then can we be sure that our reconstructed output signal will be the same as the original input signal. This is because if we were to sample at 40k Hz and we would be recording a signal that also contains 25k hurts we would innacurately record the 20-25k range and thus introduce aliasing. Therefore, to be sure that is won't happen we need to limit the band - in this case - to 20k Hz so that NOTHING can ever be recorded beyond that and thus EVERYTHING that will actually be recorded will be recorded accurately. Additionally, even if the 20-25k is inaudible to the human ear anyway, we need to introduce this limit because the aliasing will cause these waves to distort the lower frequencies that we can actually hear.

Additionally, our reconstruction formula als needs to work with that same bandlimit since only then will it calculate the correct reconstruction waveform from our samples.

## PRACTICAL Reconstruction Accuracy: Quantization
So, up until now we've basically looked at sampling and reconstruction from a theoretical standpoint, a mathematical one if you will. However, in practice the story actually isn't as perfect as I depicted it to be. 

Up until now we've established that we could easily do AD/DA conversion with 100% accuracy through the process of:

Continuous wave > Write down samples > Reconstruct wave from samples with formula.

However, this is on LITERAL paper, as in a mathematical way. What we didn't take into account is that we need to store these points not on paper but digitally on a computer. This process actually requires an extra step called *quantization* and it is with this step that some imperfections get introduced.

So what is quantization, how does it work and why do we need it?

Well, quantization is the process of mapping input values from a large set (often a continuous set) to output values in a (countable) smaller set. In our case that would mean mapping our analog continous sampled readings set (which are 100% accurate) to a set of less accurate rounded/quantized (or truncated, depending on quantizer?) values. The numbers we round to are also not random. In signal quantizing we usually choose a set of pre-determined numbers that are evenly spaced between the maximum and minimum amplitude. Each number we choose is called a *quantization level*

So, for example, let's say we chose 2 quantization levels and we happened to record a signal with maximum amplitude that was 10 and -10. In that case we would choose 10 and -10 to be the two levels analog values could quantize to. If we then had a analog readings set of [8.4564564654, -4.14545, 5.45464646] our quantized set would look like [10, -10, 10] since most quantizers simply quantize the analog values to the closest available quantization value level.

Now, there is obviously a difference between our analog set values and our quantized values. The differences between these values are called *quantization errors*. In this case that would be [1.5435435346, -5.85455, 4.54535354]. Now, important to note with these quantization errors is that if your maximum amplitude was only 0.5 and -0.5 and you had a reading of something in between the two like 0.01, that the quantizing error is only 0.49 in that case. In fact, in the [-0.5, 0.5] range we can never even have a quantize error of 5 in amplitude as we had with our first example. What this this thus means is that if you're recording low amplitude analog signals, you can actually get away with lower quantization levels than if you're recording very loud high amplitude signals since the maximum error is so much smaller for lower amplitudes than it is for higher amplitudes with the same level. This is important because quantization errors do have an impact on audio quality (as we'll see in a bit). Therefore, if you're recording something that is very loud you'll want to make sure that you have enough quantization levels (or *bit depth*) as we'll see to quantize to so that the maximum quantization errors can be minimal. In other words, the higher the bit depth the louder you can record without hearing audible artifacts that screw up your signal.

**INTERMEZZO: You can also understand the impact of quantization with images. Every image is represented with pixels. The smaller the image is the less pixels you need to represent the image accurately, the bigger the more pixels you need to display the image with the same accuracy. This is because now that apple on your image is literally bigger and thus literally requires more pixels to represent in the same way as the smaller apple in the smaller image that required less pixels to be displayed well. That's also why if you upscale small images beyond the size that they were meant to be displayed at (since at that size the pixel density is accurate enough to make it seem like the photo isn't pixely but also not big enough to accurately display the picture at anything higher than that), they start to look very "pixely".**

But the inner workings aside, why do we need to quantize our analog readings at all, though? Why don't we just store the real analog value because surely that value is not infinite so its storeable, right? Well, that is true, but you need to realize that sampling an analog value from a continuous datasource - such as a sound wave - can take on ANY value. That is, you can have analog value readings with only 4 digits like 5.014 but you could also perfectly have a value that is 6.00004578787527854887. In fact, you can have values consisting of 10000000 billion digits and beyond. In our case, as long as the maximum amplitude of our sound wave is at least more than 0 in amplitude we can literally do an infinite amount of different analog readings between 0 and the maximum amplitude. Therefore, it's entirely possible to do a random analog voltage reading that also happens to be 10000000 billion digits long. Incidentally, I don't think it's hard to imagine that storing a number that big will require some storage/bits of your computer to be able to store that (if it can even store it)...and that is just 1 single analog reading. Imagine, a second reading that is just as big! The reason that we thus quantize is because we want to **eliminate the possibility of having to store an incredible amount of digits which would overload our storage system (just like an incredible amount of samples would do TOO).**

See:
https://www.quora.com/Why-is-quantization-needed-for-digital-signal-processing
https://www.javatpoint.com/dip-quantization-concept

## Bit depth
Good video: https://youtu.be/zC5KFnSUPNo?t=290
Good chapter: https://youtu.be/cIQ9IXSUzuM?t=523
https://www.youtube.com/watch?v=IRlohQw-1DY
https://en.wikipedia.org/wiki/Audio_bit_depth
https://www.soundguys.com/audio-bit-depth-explained-23706/
https://www.lifewire.com/signal-to-noise-ratio-3134701

Now, the amount of quantization levels are actually determined by something called the *bit depth*. The more bits we allow to quantize to (is this a correct sentence?) the more possible values we incidentally allow to quantize to too. Doubling bits (why doubling bits or +8 why not an odd number of bits?) increases exponentially(?) the amount of possible values we can quantize to.

The idea with choosing a correct bit depth is that we want a high enough bit depth to minimize the quantization errors. Because, the less the values of the quantization errors are, the less impact it will have on our audio quality. These days, usually we use 16 bits and even 24 bits as those give us acceptable amounts of quantization levels that give us quantization errors that won't really noticeably affect our audio quality (given that we don't record anything anything at an insane level of amplitude).

## Quantization noise
Now, what do we really mean with "affecting audio quality" in this case. Well, very simple, quantization errors manifest themselves in our output signal as distortion. The more distortion the less resembling our output signal is to our output and thus the less quality 

// Explain here why odd harmonics cuz flatten and show graph/link => Now, the main reason that quantization errors distort a sound wave is due to the fact that consecutive values get rounded to sometimes the same values and then values after that way higher which creates kind of this band/stairstep-eque effect in some places of the waveform. Additionally, it doesn't help that all analog values that were pretty close in value would all be quantized to the same predictable value and thus our reconstruction algorithm (needs work). Look at how 1 bit you can clearly seen the qunatiozation staircase cuz only few values so of course staircase will happen cuz loads of consecutive values will qunatize to same exact value and then others might quantize to a total different ampltiude (ampltidudes spread far apart making for a high amltiude squarisation)

**NOTE: Quantization errors ALWAYS add harmonics, they inherently can never remove harmonics. Therefore, our original input signal actually is still to be ALWAYS fully found in the output signal (why?). Therefore, our input signal is still reconstructed in a 100% accurate way except for the noise. However, to the reconstruction algorithm it looks like he reconstructed the wave with 100% accuracy since he had to already work with the quantized sample values.**

Now, logically, the less our rounding errors are in value, the less distortion we will have in our output signal. Therefore, as we've just seen, reducing the distortion in our output signal is simply a matter of increasing quantization levels and thus bit depth. 16-bits and 24-bits are safe bit depths since at these depths the distortion added is so low that at the usual amplitudes we record (and listen) music at, the distortion is literally inaudible to the human ear. And even if we would MASSIVELY turn up the amplitude and have the distortion be audible, our actual output signal regardless of the quantization noise is so loud at that point that we don't even hear the added distortion content anyway.

## Low bit depth and dither
https://www.youtube.com/watch?v=zWpWIQw7HWU
https://www.soundguys.com/what-is-dither-23700/

Now, that doesn't mean that the distortion did not used to cause audible problems but that was all back in the day where bit-depths lower than 8-bit where the norm. For example, in the eras where we only could record at 5-6bit depth the distortion from quantization errors was indeed audible.

Luckily they had a solution back in the day to combat that: dithering (or "adding dither"). "Dithering" is a really simple concept and simply refers to the act of adding white noise to the original signal (so BEFORE sampling and BEFORE quantization).

So what does adding white noise do for us? Well, it's all about "masking" the distortion. With adding white noise we can easily mask the distortion created by our quantization errors making it seems as they aren't there. 

**INTERMEZZO: Remember that white noise is a signal - usually between 20-20k Hz (human hearing range) - that has equal intensity for ALL frequencies. In other words, every frequency has the same amplitude. Now, to construct white noise there are several methods but most commonly (and the easiet way) is to randomly generate amplitude values for all the frequencies between 20-20k. Random obviously means that EACH frequency has EQUAL chance to generate ANY amplitude value resulting (more or less) in a uniform MEAN amplitude distribution over the whole frequency spectrum, i.e. noticeable as a flat horizontal line on a LINEAR frequency spectrum analyzer at ANY point in time (since these signals get emitted at such a fast pace, we can only even see and hear the average and not even the values in between unless we played the white noise at a VERY brief moment sine then outliers might be visible). Now, of course, random isn't the only option. Sine sweeping and artifically constructing a non-random ideal white noise pattern with Fourier transorms (Lanczos method - https://accelconf.web.cern.ch/e08/papers/tupc103.pdf) are other options but as far as I know are either slower in generation (sine sweeping) or harder/impossible to execute or don't emulate "real" white noise (?). Also, the end result is mostly the same and in music and dithering it doesn't matter to have "ideal" white noise and maybe the randomness can be an asset (?). Also, random distribution, or pseudo random distribution of course also matters: https://www.oreilly.com/library/view/think-dsp/9781491938508/ch04.html, https://www.physik.uzh.ch/local/teaching/SPI301/LV-2015-Help/lvanlsconcepts.chm/Noise_Generation.html**

So how does that work? Well, first of all, it's important to understand that we don't have to use white noise to mask the distortion, we could use ANY waveform. For example, let's say that we had a sine wave and a square wave playing at the same time (we can see the square wave as "distortion" in this case). What we can do is literally increase the amplitude of the sine wave until we don't hear the square wave anymore. The waveform will thus also look like just a sine wave but if we look really close we can see some tiny amplitudes of the square wave in there. This is the concept. Now two problems to note here:

1) If you wanted to keep your sine wave amplitude and wanted to filter out the square wave with another wave, you could of course just add another wave and make sure that you increased the other wave amplitude in high enough loudness until you can't hear the square anymore. Now, of course in that case you've also masked the sine wave you wanted to keep so that is a big problem.
2) A sine wave requires a higher (in fact, the highest) amplitude to be able to mask other sound waves since it has so little frequency content, therefore totally masking our original sound wave. To understand that a sine wave at 1k Hz + a square wave is basically still a square wave with only a loud harmonic added at 1k Hz. And thus, to be able to make the square wave harmonics inaudible you need to make that 1 harmonic real loud. Meanwhile, if you wanted to mask a square wave with a saw wave, you don't need to do that as much since the saw wave has a lot of harmonics on its own, therefore, even if the square wave is in theory still audible to the human ear, the higher amplitude values of the saw wave fundamental and its harmonics will mask out anything the square wave has to offer. This can also be seen in the waveform that mostly shows a saw wave with only square wave frequency content if we look really close. 
3) Lastly, the wave frequency you use to mask might also determines how much in amplitude you need to increase before masking the wave you want to mask. For example if you have a low square wave, you'll need to mainly mask the fundamental but if you use a wave that has not the same fundamental then you need to rely on, then that fundamental will play next to you're masking wave kind of as a chord and thus you need to increase much in amplitude to not hear the fundamental. Meanwhile if you do choose the same fundamental, it's just a matter of increasing in amplitude as much to drown out the harmonics that make up the timbre of the square (since the fundamental itself is the same and thus doesn't need to be drown out necessarily). And of course, harmonics are less in amplitude than the fundamental to begin with so less increase in amplitude is required.

Now of course, all the above is completely useless to mask frequencies because the waves added completely changes the wave we had. So while it might mask the stuff we wanted to mask, our sound has so much added frequency content too of the masking wave that this masking is useless. This is why we need to use white noise because white noise to us doesn't sound like distortion. It sounds like...well noise and therefore, if we add it to our wave we always hear it as the same wave but with a lot of "hiss" or "background noise" instead of distortion. And of course, if we add white noise that is too loud we will also completely mask our original sound wave in which we want to mask some distortion only. However, if we can add white nois that can both mask the distortion AND have it as quiet as possible then we have succeeded in our mission of masking *quantization noise*.

Now, of course, white noise sounding like actual noise and not distortion is not the only reason why we use it to mask *quantization noise. It's also because of its properties to have equal intensity over the whole frequency spectrum meaning that it doesn't have a real fundamental tone, it's all fundamental tones. Therefore, as we've just seen, we don't need to choose at which pitch we have our white noise playing since it will still mask any harmonics and distortion at ANY frequency just as much no matter at which "pitch" it plays (it can't even play at a pitch, unless you draw it in FL studio, but every pitch is the exact same white noise).

But okay, let's hover back to our quantization and adding white noise to it (though, remember that we can add ANY wave to mask our quantization error but that we choose white noise for above reasons).

So, when we add white noise to our sampled values we are in reality altering the amplitude values of our sampled amplitude values. For example, if our input signal at a certain sample point is 5 amplitude BUT our white noise might be -3 amplitude at that point, then the final sampled value will be 2 in amplitude. Incidentally, what that thus means is that our sampled values might quantize to different levels due to that white noise having added to or subtracted from the original sampled amplitude value. Then for the next sample point there is going to be a less predictable quantization level too since white noise is such a complex waveform that it fluctuates so fast and much in amplitude value that at the next sample point our white noise might be at a completely different level than -3, i.e. there is no correlation anymore between quantization values (like linear going up, staircase, etc.) In other words, it *makes quantization error less predictable*. In fact, since white noise amplitude values are also generated randomly, it even makes it completely random (though it's mainly the unpredictability than the randomisation that is important).

Now, of course, how can randomizing quantization errors ever be accurate? Well, it's true that we might quantize to totally random levels per sample, totally screwing up our input signal, the trick is to have our white noise maximum amplitude not be too high, yet still high enough to drown out the qua,tization error we had without the white noise. Intuitively, this makes sense because the louder we turn up noise the less we can hear from our sound wave, right. But this also makes sense on a more scientific level since if your sample amplitude values can only fluctuate with maximum 0.5 amplitude in difference (since your white noise might have a +0.25 and -0.25 max amplitude), obviously the value our sample we quantize too will still be close to the original value we would have quantized to. Because, if our white noise had like +100 -100 ampltiude, then our samples could possible vary 200 in amplitude and thus quantize to whole different level of quantization which is indeed totally inaccurate and totally screws up our input wave. 

Now, I don't know exactly how loud or how quiet dither should be to exactly add as much noise to fully randomize quantization error, remove stairstep and thus remove disortion but I'm sure it can be mathematically derived. Also, the lower your bit depth the louder your white noise needs to be because there are very little quantization levels and they are spread far apart, therefore to make sure that we don't get consecutive values quantizing at the same levels we need to modify them high enough in amplitude that they do quantize to different levels. Of course, this means less audio quality and possibly, depending on how little bit depth, audible/very audible noise and maybe even very little actual sound but that's what's needed to not hear distortion and thus still our true input sound (but with noise of course). This is again why 16 and 24 bits are safe because they have so many quantization levels that first of all the quantization errors will be small but also, second of all spanning a few different quantization levels doesn't require much change in amplitude at all, thus very little noise (with very little difference in amplitude in comparison to what it would have originally quantized to) is needed to have a very varied palette of quantized values that will never(?) produce any stairstep/clipping whatshowever and thus still be accurate. 

Now, second to last thing about dither. Dither can be anything, people can *noise shape* dither, like use triangle dither and stuff that will actually *noise shape* the noise into the higher frequencies (if have time look up how that works) where noise is generally less noticeable then in the lower frequencies. Also, dither can be balanced with distortion because to eliminate all distortion you need the "highest" amplitude in noise (because anything lower will have distortion). Therefore, to have less noise (but again have a bit more distortion which may or may not be audible) people sometimes balance the white noise amplitude and the amount of distortion it really masks as sort of a trade off.

## Signal-to-noise ratio (SNR)
https://www.soundguys.com/audio-bit-depth-explained-23706/
https://www.lifewire.com/signal-to-noise-ratio-3134701

Now, all this said though, is that you should really not worry too much about dither. As you can see here https://www.youtube.com/watch?v=cIQ9IXSUzuM& in the dither section, 16 and 24 bits have literally inaudible disortion. In fact, they have a *signal-to-noise* ratio of respectively 96db for 16-bit and 144db for 24-bit (or is that for *noise floor* with dither? Either way it's not going to be too fluctuating). What that means is that for 16-bit, the actual signal is 96db louder than the *noise floor*. And thus, ,if your signal is not even 96db loud (which is already very loud) you won't even hear the *noise*. On top of that, even if the noise becomes as loud as for a human to be audible, the actual signal is already so loud that it completely drowns out - to our ear anyway - the noise.

## Conclusion
So to conclude, should we still worry about samplerate and bit depth in a practical setting? Well, yes but not in depth. 

First of all, you should know that in order to have a quality recording you'd want to have a samplerate of at least 44.1k Hz and a bit depth of 16-24 bit. However, you usually don't need to worry about that since most modern audio interfaces will already do that out-of-the-box obviously. Even if processing your audio with non-linear effects (which can cause aliasing) you don't need to worry since our soundcard (and any good soundcard) has a bandlimit of 20k anyway (?).

Secondly, you also need to be high-level aware of what recording at HIGHER rates and bit depths can do for you. They do NOTHING for audio quality but they can be useful if you want to later manipulate and add (non-linear) effects to the audio. See "Sampling" for exactly what they can do for you. Note also that in terms of intermodulation distortion (See "Intermodulation Distortion"), a higher sample rate is disfavored and that if you're recording at a high sample rate (and your mic can pick it up) and then downsample (without filtering) you'll get a ton of aliasing of these higher frequencies (see "Aliasing", the distortion part, it's basically the same).

Thirdly, you need to be high-level aware of what recording at LOWER rates and bit depths can do for you. You need to know that these will audibly lower audio quality. Generally, when you see samples out there that are recorded at a sample rate of less than 44.1k Hz and/or a bit depth of 8-bits and lower you need to realize these are low bandwidth/resolution recordings. That said, they CAN be used if you like how they sound and if you like the distortion that both aliasing and/or bigger quantization errors bring. In fact, often people might *bitcrush* (https://en.wikipedia.org/wiki/Bitcrusher) a perfectly fine sample or synth sound as a form of saturation/distortion because these effects both add (and in case of *downsampling* also remove) harmonics thus make a sound warmer (what is warmer?). To read more about how people use both sample rate reduction and resolution reduction as effects read "Common FX explained" and "Sampling".

Lastly, you do need to be aware about *aliasing* and when it can occur, what it sounds like, when it is a problem and what can be done about it. We touched on it here, but to really learn about it, go to the article "Aliasing" and "Sampling".

## FAQ
### What about Synthesis & MIDI? Do they suffer from the same sample limits as audio?
http://digitalsoundandmusic.com/6-1-3-midi-data-compared-to-digital-audio/
https://www.reddit.com/r/WeAreTheMusicMakers/comments/3o0103/eli5_analog_synthesizer_vs_digital_synthesizer/
https://www.reddit.com/r/synthesizers/comments/9q1hng/i_think_im_hearing_the_shortcomings_of_digital/
https://en.wikipedia.org/wiki/MIDI

> See Synthesisers

First of all, there is a difference between an analog synth and a digital synth. Now, one would think that that difference is that an analog synth is hardware and a digital synth is software. This couldn't be further from the truth. Both analog synths and digital synths can be hardware (though a true analog synth cannot be software). The difference lies in the fact in how they generate their sounds. You see, an analog synth does this with a literal electric circuit, i.e. it's generating sounds literally through analog equipment and electricity. The sound it generates is therefore PERFECTLY continuous and the sound waves that get generated aren't prone to aliasing no matter what. A digital synth on the other hand generates its sounds through mathematics and a digital circuit. The sounds doesn't come from real electricty but rather from mathematical calculations to represent the wave needed (like in 1's and 0's). And because of that, the sound wave generated by a digital synth is not continuous, it's also just an array of discrete amplitude values that are calculated at an accuracy of 32-bit that then gets send to a DAC and to the speakers. A 


lookup the synth dr guy with his floating point what was it about???

what is hard clipping and what is 16-bit audio buffer????


the wave and  and  both can be hardware synths but the way they generate sounds is different. As you can guess one generates
so i guess d to analog converter does high pass at 20k but since already recorded, we hear the aliasing in the audible range because of the higher frequencies due to the synth if we didn't high pass it
so digital synths don't suffer bit depth i guess cuz they can construct a mathematical wave, they don't need to rely on samples recorded? Or do they suffer from bit depth or less?
bu also low pass after tho???? aftersynthesis so why still aliasing ,lookup if synth does low passing too
> See "Synthesis" for full explanation on synthesis and MIDI.

So you could ask yourself the question, what about (software, so not analog but the concept is the same) synthesizer output audio? Surely, to hear the sounds from those we should also do some conversion magic right?

Nope, we actually don't need to. Why? Well, because a synth works with MIDI (see "Synthesis"). MIDI is not audio but just instructions that a synth can interpret to generate its final sound (stuff like NoteOn() and NoteOff() and aftertouch value information per note etc.). And thus, from the moment a synth has its MIDI information and we hit "play", it will interpret it and then, just like a DA converter, will send electric voltages that represent a continuous wave based on the MIDI information and its "patch" settings. 

An important note to thus make and understand here is that sample rate and bit depth are totally irrelevant to a sound generated by a synth (for both analog and digital synths, unless you would be literally recording the output of an analog synth with an audio interface lol). This is because, in the other camp, so in DA conversion with digitally stored audio, you would always need to have quantized sample points to be able to construct electric voltages that resemble a continuous wave and are send to the speakers. How else would you construct an electric wave signal that was the original sound wave? There is literally no information than the samples but since the samples are quantized we can't be 100% accurate in reconstruction. *A synth on the other hand doesn't need quantized sample points at all* to construct electric voltages that are send to the speakers. All it needs is MIDI information - which is just a list of numbers and settings - and "patch" information which is also just a list of number and settings.


## If 44.1k Hz sample rate (and 16-bit bit depth) is more than enough to cover all of human hearing, are their any benefits to recording at a higher rate/bit depth?
https://www.kvraudio.com/forum/viewtopic.php?t=387328
https://youtu.be/-jCwIsT0X8M?t=300
https://en.wikipedia.org/wiki/Undersampling
https://en.wikipedia.org/wiki/Oversampling

> See "Sampling" for a full answer on this.

Sampling at a SIGNIFICANT higher rate than the Nyquist rate is called *oversampling* (the opposite, though doesn't have to be significant, it's called *undersampling*). That is, at a standard bandlimit of around 20k Hz, if we were to sample at a higher rate than our standard 44.1k Hz, like 96k Hz, we would thus be oversampling.

So why would we want to do that ever? Well, for the sake of consumers there is actually no reason at all that a CD has an absurdly high sampling rate. In fact, most speakers aren't even capable of reproducing the frequencies that those absurd sampling rates can record (and we cannot even hear them). 

That said, there could be a potential problem with the speakers playing back audio since they might not play it back in a linear way (in this case that would mean input =/ output). There might be some non-linearities such as distortion due to intermodulation. () But, that's all to worry about. For music production (In a DAW shit is linear so no problem), also intermodulation distortion only happens from two tones so never can be one like intermodulation. But again, please refer to the "Sampling" article for a full answer.

// TODO what about higher bit depth? Why? Literally only for louder or other things?

## What about sample processing such as up and down sampling & audio quality?
> See "Sampling".

## What about bitrate & audio quality (.mp3 lossy vs .wav lossless)?

## General sources
https://www.bax-shop.be/blog/studio-recording/sample-rate-en-bit-diepte-betekent-geluidskwaliteit/
https://www.izotope.com/en/learn/digital-audio-basics-sample-rate-and-bit-depth.html
https://www.reddit.com/r/explainlikeimfive/comments/4d4krv/eli5_what_is_the_difference_between_sample_rate/
https://charlottekeating.files.wordpress.com/2012/11/bit-depth.jpg
https://www.youtube.com/watch?v=yWqrx08UeUs
https://www.youtube.com/watch?v=U2mwXiJqAgA
https://www.youtube.com/watch?v=cIQ9IXSUzuM
https://www.youtube.com/watch?v=zC5KFnSUPNo&t=339s
https://www.sciencedirect.com/topics/computer-science/quantization-noise
https://www.sciencedirect.com/topics/engineering/dither-signal
https://www.sciencedirect.com/topics/engineering/nyquist-frequency
https://www.sciencedirect.com/topics/engineering/samplerate
https://www.youtube.com/watch?v=-jCwIsT0X8M

## TODO
- still add why sampling at higher than 44.1k Hz and more than 16 or 24 bit depth is useful (pitch shifting time stretching etc.) Also why 48k and vice versa not easily convertible.
dithered quantizaion noise is higher power than undithered: https://www.allaboutcircuits.com/technical-articles/quantization-nois-amplitude-quantization-error-analog-to-digital-converters/ 
- Find the article that discussed a lot of interpolation techniques (such as zero order hold, which connects dots straight horizontal line extended, linear, which connects dots with a line going towards the next sample point, can look real smooth from far and enough points, etc.: http://www.eie.polyu.edu.hk/~enyhchan/audio_midi.pdf)
- Add more detailled explanation about how digital converts back to analog (with like electric signal it generates and then sends to speaker)
- Talk about 44.1k buffer because how in practice bandlimit like eletric circuit can't be trusted fully since it might still let through frequencies a bit beyond the theoretical limit, talk about why 16-bit is standard CD (or 24-bit)
- Talk about filter types after reconstruction like anti imaging filters like smooth filter, brickwall filter.
- Intermodulation = aliasing kind of?
- https://en.wikipedia.org/wiki/Gibbs_phenomenon Gibbs effect? The FL studio Monty guy talked about/mentioned it

## Unprocessed notes

look up! is that a bad thing or good thing what does it mean? at 14:50s
frequency masking?

Sample rates and bit rates higher than human hearing limit necessary why?
24 bits 144 db and 16 bits 96 db
say something about accuracy here.

Therefore, we want to have these harmonics to be inaudible and thus we need to choose a high enough bit depth. Now, of course, even with high bit depths, the higher the amplitude, the more prominent the harmonics will become too and eventually they'll become audible. But still, since at that point the actual wave is so loud at these bit depths that the added harmonic content of the quantization noise will still (probably) not be heard.


shaped in higer frequency, triangle shape best why?
also dither don't really matter in the 16-bit and beyond era, but as we said it's insurance.


if unlucky stil stairstep? But we need to be extremely unlucky



not only reason so much frequncy content that


because adding white noise is equal intensity across the whole frequency spectrum it can be literally used to first of all, as you can see in the video, adding white noise alters our sampled values. 



but will our waveform still be accurate, yes if added white noise quiet enough



Effectively, what white noise is doing is replacing the staircase-esque banding/clipping and replacing them with more peaks and throughs.
could have added any other wave besides white noise ofc but then it's not sound as white noise



**TODO: Is signal-to-noise ratio better with dither than without?**

different ways to shape, triangle shape is best
the webfotn smoothing anti aliasing

error introduces noise which is called quantization noise


lossy compression? what is that? mp3 and stuff?

what is bitrate?

On a computer we can't do that because we actually need to store these samples digitally. And to store the samples digitally there is actually an extra step required: quantization.

so this formula is perfect but not in practice but not in real
So anyway. We forgot something so introduces noise but still mathematically accurate just in practice

**TODO: This section needs work. Like, add here which harmonics, also add that the harmonics change with sample timing or with different bit depth or that in the latter case we just have less of the harmonics. Also, is the connect the dots wrong in the above first video i guess so. There should be ripples, right? Like ripples like a square but yeah technically that is squared off. (odd/"squared off"/like a square wave has only odd harmonics???? I don't know if this is true at all). According to last video, yes ODD harmonics since suqared off get added but why only odd? cuz squared off, but i saw a paper here http://www.scielo.org.mx/pdf/jart/v7n2/v7n2a3.pdf in conclusion said that NOT ONLY odd harmonic content but also other content, but looks like less prevalent though??. also, are the harmonics more prominent low bit or are there more harmonics and/or are more prominent???**

but how dones reconstruction know that it should be flat there?
tell here that NOTHING gets removed from input harmonic wise onnly added so reconstruction is still 100% accurate in a sense. Why not removed never? cuz original would be more round = less harmonics and quantized always more squared = more harmonics? also talk here about how harmonics get added, like how the wave output wave defers from the input wave i guess peak samples will often be quantized to the same value so reconstruct the line between i guess it's more suqared off to be able to go through these two points?

0db is usually a reference level, reason we do negative db is because we might set a highest peak to 0db and anything lower in volume is negative db obviously. Reason we don't choose any positive db is because what db would we choose? Like 50db? and then compare stuff to 50db? That doesn't make real sense so we set 0db as a reference db. Now in mixing everything can be below 0db of course, which is what we call headroom. However, 0db can also reference one loudest noise that we then compare other noises to, if other noises are positive in db it means these are louder and if the are quieter they will be negative in db, if we were to choose another sound with different db then all the comparisons of course need to be recalculated.

https://www.scienceabc.com/pure-sciences/why-negative-decibels-are-a-thing.html => this article says when talking about DB if we're talking about general context then 0db is lowest a human can hear and then everything is compared to that. If in mixing environment 0db is the level at which stuff would clip i guess and thus all sounds in ur song are compared to that in fl studio the faders are set to -6db right?

only sample signal if band limited why:
https://www.youtube.com/watch?v=ADQt0ZNt0jU

we can ALWAYS record ANY wave no matter how fast cuz at ANY sample rate that point will ALWAYS fall on a point of that fast wave you see no matter what, it's continous there are no gaps in the wave.

an IRL sound wave is an INFINITE set of points (i.e. continous). How would you go about converting AND storing an INFINTE amount of points? You can't.

there are two core things happening. First of all, we have sampling and second of all we have quantization.

But there is a problem, since a sound and (basically anything happening IRL) is continous, it means the wave depicting it is literally made up of an infinite amount o

We can't just convert an analog signal. A wave that depicts a vibration is continous, meaning that it is made up of an infinite amount of points. There is no way

so bitrate is like unrelated to sampling so we don't care really.

according to FL guy, so not only even bits that get double or plus 8, aha! so like we don't go from 1-2-4-8 in between like 5-6 bits als existed but maybe these roundings like 8 and 16 and 24 are easy to calculate with??

What this means is that everytime a signal gets emitted by a generator ANY frequency basically has an EQUAL chance to be emitted or not. So for example, maybe in one emission 20.0001 Hz might be emitted but maybe 40.5454 Hz might not. Not only that, every frequency emitted is equally intense (more or less meaning they are the same in amplitude). Therefore, since every frequency has an equal chance to be emitted at equal density, a LINEAR frequency analyzer will more or less show a flat line on average (not fully since sometimes frequency briefly are less in intensity when not emitted or more since they got emitted more than average). And thus, if you would take samples of the frequency spectrum and average them out, the more samples you have, the more our average will actually look like a flat line. Now, how white noise gets implemented in practice is something else since true white noise generation between 20 and 20k Hz is of a continuous nature (infinite amounts of frequencies that could be generate). However, the concept stays the same. Also, to go on a bit of a tangent. Pink noise is different to white noise as in that the amplitudes of the higher frequencies are less since humans are more sensitive to that area. With white noise we would hear the higher frequencies more but with pink noise we hear all frequencies equal.**