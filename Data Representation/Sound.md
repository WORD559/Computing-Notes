# Sound #

The real world is an analogue signal. There is (sort of) a lack of precision in the real world. You could have 10000Hz, or you could have 20000Hz, or you could have 15000Hz, or 12345.6789Hz. At the same time, the sound is continuous, a smooth waveform.

[Analogue Wave](analogue.jpg)

Computers are very precise. There is no room for it being a different to what is an acceptable value. This infinite variationand smooth wavelength is not possible in a computer. Digital signals cannot represent analogue data perfectly.

When computers record sound, they do it with a sampling depth and a sampling rate. The sampling rate is how often the sound should be checked for its value, and the sampling depth is how accurate the value should be. 

[Digital Wave](digital.jpg)

The output of this would be 11001001

The digital wave looks somewhat similar, and would sound somewhat similar, but not a lot. You'd get very little resemblance. 

We can make it more accurate by either increasing the sample depth, so that there is more accuracy in each sample, or increase the sample rate so that the samples are more frequent (which should make the sound look more wavelike).

--------------

When we sample sounds, we use Nyquist's Theory, which means we have to pick a sample rate in Hz that is > (not >=) the highest frequency we want to sample, our recorded analogue waveforms will ALWAYS look like waves. 

If we recorded at the same rate as the frequency, we would have a completely flat wave. If we recorded at a rate of double the frequency, we could potentially land on the start, middle and end of one cycle, and get a flat wave. So long as it is greater than double, it is guaranteed to make a wave.
