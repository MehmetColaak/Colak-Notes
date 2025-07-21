## Conceptual Framework
This section details the concept and design features of the Embracing Sphere installation. It describes the main conceptual components chosen and explains how they integrate to create an audio-tactile environmental storytelling experience.

Embracing Sphere aims to combine key theoretical constructs that have been covered in Chapter 2 (environmental storytelling, multi-modal perception, and audio-tactile interaction). This vision directs the design and the implementation of the Embracing Sphere.

DIAGRAM

The above diagram shows conceptual elements of the Embracing Sphere with "technical" and "artistic" categorizations. This diagram shows my consideration points when creating the experience such as "How audio-tactile system is going to displayed to the audience?" and "How much narrative should I enforced in the experience?". These considerations basically constrain my technical and artistic decisions according to the requirements in exhibition thematically and technically. 

For example the audio-tactile display equipments is chosen with consideration of collaborative exhibition setting of Ars Electronica Festival Campus Exhibition. Therefore instead of a speaker array, a headphone and 3 bass shakers are chosen for audio-tactile play system. In this setup headphone is displaying binaural mix of audio channels composed in ambisonic format for 3D audio.
## Procedural RIR Generation System
This section will detail the procedural RIR generation process in Embracing Sphere. Every different surrounding of us has different acoustical parameters and in time domain has different characters. Some enclosures has more dull and short response while other can be bright and long. This characteristic differences has covered in section 2.2.2 Room Impulse Response Measurement Methods. 

Utilizing this characteristic differences may apply contrast and environmental shifting abilities to auditory face of Embracing Sphere. Room impulse responses can be archived and used in demand with a RIR bank system that changing RIR file in convolution reverb but to artistically I chose more aleatoric way of generating RIR files with some parameters introduced in advance (procedural generation).

Sabine formula that covered in 2.2.1 Definitions for Room Acoustics is simple enough to implement and outputs big enough range values to hear the difference. The RT60 parameter generated with sabine formula is used in RIR generation module.
$$T_{60} = \frac{0.161 \cdot V}{A}$$
In detail, sabine formula needs effective surface area, volume variables to output RT60 value. Randomly generating numbers for an imaginary room dimensions can enable us to calculate an effective surface area and volume.

IMAGE

As seen in the figure \ref{} 4 random number (3 for dimensions of the room, 1 for overall absorption coefficient) generated using Max/MSP random number generator object, with the scale object parameters the output numbers limited between 3 meter to 20 meter in width and depth and 3 meter to 4.5 meter for height of the imaginary room. Then rest of the expression objects are implementing Sabine formula into module. The output defines the length of the RIR file.

RT60 alone is not enough to create a RIR. At the same time we need to generate a gradual fade and filter out envelopes to imitate an absorption slope. Subtractive synthesis came into formula at this point, basically gradually filtering and turning down the volume of a white noise with subtractive synthesis approach can be utilized in procedural RIR generation.

IMAGE

Flowchart above in the figure \ref{} showing high level process flow in the procedural RIR generation. The output of this process is not a simulation level or mentioned RIR capturing methods level realistic but this primitive approach generates fast realtime RIR files to use in convolution reverb.

With high level explanation of procedural RIR generation, next section will cover haptic and audio content design and playback system details.
## Audio-Tactile Content Design and Playback System
Embracing Sphere is developed as an interface rather than a artistic content. Although it is going to exhibited in Ars Electronica Festival - Campus Exhibition, the system developed to have adaptability so audio and haptic content of the system can be authored and updated.

The artwork can be seen as a theme park train ride or commercially named "4D Cinema" experiences. Nonetheless this research is investigating audio-tactile interfaces in the main focus. There is a narration to follow that is going to be detailed in the next chapter but the main drive here for the Embracing Sphere is feeling the environment and make audience interpret their own environmental storytelling cues. 
### Audio Content and Playback System Technologies
Collaborative exhibition situations taken into account, we decided to choose a regual headphone to not interfere with the other artworks. Following that decision, multi-channel playback system needs lowered dramatically.

In this plan 2 channel audio and 3 channel haptic signals composed for the experience. For the length of the experience, average audience attention span without visual motion graphics considered and according to the researches around this topic\cite{}, approximately 8 minute experience planned.

Stereophonic audio first patented by Alan Blumlein, a renown electronic engineer with his inventions in telecommunications and sound technologies\cite{}. The headphones we still using now utilizing same principle of the first stereophonic system. In the vision of creating audio-tactile virtual environments stereophonic compositions is not enough with the spatial needs of auditory domain. Thus "binaural" mixing have chosen to take leverage of spatial audio technologies such as ambisonics.

Binaural mixing, unlike traditional stereo, recreates the natural listening experience by profiling how our ears receive sound in three-dimensional space. This technique utilizes Head-Related Transfer Functions (HRTFs) to simulate how sound waves interact with our head and ear cone before reaching our eardrums. Binaural audio mixing process audio with these psychoacoustic filters to create convincing spatial perception when played through headphones. With binaural audio listeners perceive sounds as coming from specific locations around them\cite{}.

For being format-agnostic i the further projects, the main content will be composed in ambisonic format. Unlike channel-based surround sound systems that assign specific speakers to discrete audio channels, ambisonics captures and reproduces the complete spatial sound-field with spherical harmonics mathematics. Ambisonic recordings can be decoded for any speaker configuration or downgraded into binaural format for headphone playback for maintaining spatial accuracy across different playback systems\cite{}.

IMAGE

An ambisonic format audio file appears as a multichannel audio file in DAW software just like any other channel-based format, but it requires a decoder to correctly route the information in the multichannel audio file to specific speakers in order to play the audio file as desired.

For the Ars Electronica exhibition, a pure-data patch developed for binaural decoding and convolution DSP processes. Mentioned pure-data patch will explained more in the next chapter "4.2 Software Development" section.
### Vibrotactile Content and Playback System Technologies
Vibrotactile content creation in Embracing Sphere combines 2 different approach as sample based content creation and synthesized content creation. The same approaches derived from traditional sound design practices but focused in low frequencies, constrained by vibrotactile display and human haptic perception limits.

IMAGE

Main vibrotactile actuator shown in figure \ref{}, 50W 4ohm voice coil actuator specified in the spec sheet as output frequency between 10Hz and 80Hz with a resonant frequency specified as 30Hz. A signal that will be displayed through this actuator should be in that frequency range. Therefore a sensitive geophone (Lom Geofon) used for sample based approach in vibrotactile content creation.

IMAGE

Lom Geofon product spec sheet indicates frequency response between 10Hz and 1000Hz with resonant frequency at 14Hz. This frequency response specifications meets our requirements. The specific microphone mentioned in preceeding chapters this microphone mentioned and used in sampling and documenting low frequency vibrations on solid objects such as a metal bridge shown in the figure \ref{} and PlayStation 5 gamepad DualSense shown in the figure \ref{}.

The plan is collecting as many solid vibration textures as possible, editing and displaying these vibrations through voice coil actuator array which in proposed setup 3 voice coil actuator around different positions of the audience to achieve spatial perception in the vibrotactile display as audio playback system.

Within this plan utilized softwares and more details in hardwares will be covered in next chapter "Implementation".
## Narrative Structure
To effectively communicate in this section, generative adversarial networks (GANs) are utilized to create storyboard visuals that help readers understand the narrative structure and progression of the installation. These AI generated illustrations serve as visual references that can convey the abstract concepts and environmental transitions that occur during the Embracing Sphere experience.

IMAGE

The Ars Electronica Festival theme in 2025 is selected as "Panic: Yes/No?". To match the theme, narrative content is shaped around a claustrophobia and drowning.

The experience is plays a looping sound of bridge rumble noticeable in close proximity to the artwork. When the audience decide to sit the seat, the main narrative experience starts.

In first seconds of the experience, opening with first person character perspective, an individual sits on a bench on the metal constructed bridge, listening to crows in the cold, cloudy winter afternoon.

IMAGE

Then a car approaches, opens the window next to the passenger seat, and honks once. That imminent honk starts flash scene changes, and with each scene transition, we hear the honk sound in a new environment. After this short flash scene sequence, our character decides to get into the car.

IMAGE

They close the door and immediately feel isolated from the outside world, losing the vibration of the bridge as the car starts to accelerate.

IMAGE

After a short acceleration, the car gradually starts to drive out of the lane. Eventually, the car jumps off the bridge and falls into the river.

IMAGE

The car starts to fill with water and is swollen by the river. Claustrophobic scene cues with struggling to **breathe**, heavy pressure from bottom to head. After a short time of struggling, a state of tranquility arrives.

IMAGE

In this tranquility, the first and only voice line is introduced: "I've seen things, you people wouldn't believe." This line is inspired by the famous monologue in the Blade Runner movie directed by Ridley Scott. Just like the horn sound, the word "thing" in the voice line drives flash scene sequences with louder and faster transitions.

IMAGE

IMAGE

IMAGE

Our character witnesses past memories or scenes of their life and accepts their fate, falling into abstract space.

IMAGE

Eventually, they regain consciousness, floating on the river with heavy breathing and waves splashing on him. The experience initiates an end loop that plays looping wave and breathing sound cues in the river until the audience stands up and leaves the experience.

IMAGE

Within this story, I, as the author, aimed to convey as many environments as possible. Creating a narrative around the "Panic: Yes/No?" theme, I chose to explore my own instinctive panics and fears. The story is written with little to no voice-line interruptions, with the only voice line elevating new flash scene introductions.

For interactivity and playback structure, I planned two looping states and one fixed state for the playback system. This system enables the audience to first feel a glimpse of the experience through their feet when they approach the artwork. Later, the experience starts intuitively, and after the fixed state ends, the system transitions seamlessly to an ending state loop.
