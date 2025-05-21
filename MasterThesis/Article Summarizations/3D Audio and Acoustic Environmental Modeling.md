### Where? Why?
I choose this article to get a written practical resource for my proposed artwork. To give technical and practical perspective while I talk about my artwork I thought this article would help me to conceptualize and validate my approach.
### Introduction
This paper describes the 3D audio and acoustic environment modeling technology developed by Wave Arts Inc. It gives a tutorial on 3D audio and also describes implementation details about Wave Art 3D tech.
### What is a 3D Audio
A 3D audio system has the ability to position sounds all around a listener. The sounds are actually created by the loudspeakers (or headphones), but the listener’s perception is that the sounds come from arbitrary points in space.

Audio localization on conventional stereo systems is limited. Generally audience cannot position sounds to the sides or rear of the listener, nor above or below the listener. A 3D audio system attempts to do just that.
### How Does 3D Audio Work
To answer how 3D audio systems work, it is useful to start by considering how humans can localize sounds using only two ears. Hearing event in space happens with the pressure differences in the air. A sound generated in space creates a sound wave that propagates to the ears of the listener. When the sound is to the left of the listener, the sound reaches the left ear before the right ear and thus the right ear signal is delayed with respect to the left ear signal. In addition, the right ear signal will be attenuated because of “shadowing” by the head and attenuation of the air.

We unconsciously use the time delay, amplitude difference, and tonal information at each ear to determine the location of the sound. These indicators are called sound localization “cues”.

The transformation of sound from a point in space to the ear canal can be measured accurately; the measurements are called head-related transfer functions (HRTFs).
### How does 3D Work on Loudspeakers
When reproducing localization cues to a listener, it is important that the left and right audio channels remain separated, that is, the left ear signal should go to the listener’s left ear only, and the right ear signal should go to the listener’s right ear only. This is easy to achieve when the listener is using headphones. When using loudspeakers, however, there is significant “crosstalk” between each speaker and the opposite ear of the listener. Fortunately, it is possible to build an elaborate digital filter, called a “crosstalk canceller,” that eliminates crosstalk but with the downside of expecting audience in a certain position called "sweetspot". 

### Acoustic Environmental Modeling
Acoustic environment modeling refers to combining 3D spatial location cues with distance, motion, and ambience cues, to create a complete simulation of an acoustic scene.
### Reverberation
When an object in a room produces a sound, a sound wave expands outward from the source reaching walls and other objects where sound energy is both absorbed and reflected. 

Technically all reflected energy is called reverberation. Assuming a direct path exists between the source and the listener, the listener will first hear the direct sound, followed by reflections off nearby surfaces, called early reflections. After a few tenths of a second, the number of reflected waves becomes very large, and the resulting reverberation is characterized by a dense collection of soundwaves travelling in all directions, called diffuse reverberation. The time required for the reverberation to decay 60 dB below the initial level is defined as the reverberation time. Generally, reverberation in a small room decays much faster than reverberation in a large room, because in a small room the soundwaves collide with walls much more frequently, and thus are absorbed more quickly, than in a large room.

Reverberation that contains a lot of high frequency energy in the decay is associated with rooms that have hard, reflective walls, which do not readily absorb high frequencies. Similarly, reverberation that is dull sounding is associated with rooms that contain soft materials, such as plush carpets and drapes, which readily absorb high frequencies. In this manner, reverberation imparts useful information about the composition of the surrounding space.

Reverberation is also important for establishing distance cues. In a reverberant space, when the distance between the source and the listener is increased, the level of the direct sound decreases considerably, but the level of reverberation does not decrease much. Thus, the level of direct to reverberant sound can be used as a distance cue, with dry (non-reverberant) sounds perceived as being close, and reverberant sounds perceived as being distant.

Simulating reverberation is essential for establishing the spatial context of an auditory scene.
### Air Absorption
When sound propagates through air, some sound energy is absorbed in the air itself. The amount of energy loss depends on the frequency of the sound and atmospheric conditions. High frequencies are more readily absorbed than low frequencies, so the high frequencies are reduced with increasing distance.
### Object Occlusion
When a sound source is behind an occluding object, the direct path sound must diffract (bend) around the occluding object to reach the listener. Low frequencies with wavelengths larger than the size of the occluding object will not be affected much by the occluding object. High frequencies with wavelengths smaller than the size of the occluding object will be shadowed by the object, and will be greatly attenuated.

