# Embracing Sphere: Auditory Environmental Storytelling with Audio-Tactile Playback Systems
## Abstract
Conveying a story through the environment is a known technique in multiple media domains. Blood stain under the door, footstep trails on snow and broken chains next to a beware dog sign; all those flash scene descriptions are an example for environmental storytelling. Heavy reliance on visual cues defines the limitations of current methods in environmental storytelling. Utilizing multi-modal stimuli and 3D audio volumes for enhancing environmental storytelling remains niche and open for new perspectives in storytelling and narration through the environment. 

This research explores the integration of haptic feedback and acoustic modeling methods. Haptic feedback systems mostly used by video games, racing simulations and interactive art installations and haptic signals are mostly vibrations that are transferred by low frequency audio signals to create pulses on haptic actuators. Complementing tactile experience, Room Impulse Responses (RIR) utilized as a method of capturing acoustic properties of an enclosed volume/space later to use in reverberation(specifically convolution reverbs) to reconstruct the same acoustic responses while simulating different materials. Combining these distinct modalities such as tactile pulses and acoustic simulations offer a novel way to represent environmental snapshots purely through non-visual interfaces.

Building on this potential, a multi-modal stimulation scenario using simultaneous audio signal playback driven by a speaker array incorporating procedurally generated RIRs and a bass shaker (transducer) will be this article's foundational practical method. 

This applied work investigates the current state and the potential of such multi-modal experiences in conveying environmental information. Proposed artwork designs, implements and evaluates an interactive audio-tactile system capabilities of procedurally generated environmental snapshots for storytelling purposes.
## Keywords
	audio-tactile, vibrotactile, environmental storytelling, multi-modal
## Introduction
Virtual environments as narrative spaces, represents a novel way to tell a story or convey a specific feeling to the audience. Unlike traditional storytelling methods that rely on delivering a story through dialogue, cutscenes or text dumps; environmental storytelling operates more subtly.

To effectively highlight an environmental storytelling, it’s crucial to weave narrative elements seamlessly into the virtual environment that evoke emotions and encourage players to question their surroundings. The design of virtual spaces like their size, shape, flow, connectivity and materials can convey a narrative meaning. The layout of the virtual environment can guide the player along a specific path, revealing information sequentially or create feelings of safety, exposure or confusion. The environment becomes a silent narrator, communicating with the audience through carefully crafted, immovable details that enhance immersion and improve the narrative experience(Dolinski, 2025).

Due to interactive, exploratory and emergent capabilities of video games in storytelling, environmental storytelling is practiced more often especially after video game industry's increased popularity(Cachón-Ramón et al., 2023). While this practice is increasing, the auditory domain of environmental storytelling remains understudied. This thesis focuses specifically on the auditory dimension of environmental storytelling practice.

Movies, video games and interactive art installations often utilize different human sensory fields simultaneously. Understanding and leveraging this multi-modality is crucial when contributing to these mediums as an artistic individual or researcher.

With this multi-sensory understanding, this research will further investigate the interplay/crossplay between auditory and tactile feedback within environmental storytelling. The aim is to explore how audio-tactile experiences can enhance immersion, evoke emotional responses and create richer, more embodied narrative contents for the audience.
## Background and Motivation
### Multi-Modality
Modalities, the plural of modal, is a term primarily related to how media is presented, its form, or its mode. Basically, modalities are modes, a manner, way or method of doing something. Multi-modality refers to the interplay between different modes(Kress and van Leeuwen, 2001). 

The term "modality" is studied across diverse disciplines such as linguistics, media studies, semiotics and cognitive science. Each examining different aspects of representation, communication or interaction. In the context of human-computer interaction(HCI) this article uses modality term as specifically referring to sensory channels or the distinct forms of stimuli like auditory and tactile feedback.

Through this focus modality can be broadly understood as a distinct sensor, channel, system or manner through which information is represented, perceived, processed or exchanged.

The strategic combination of multiple modalities is often driven by the goal of creating more effective, intuitive, and engaging user experiences. Presenting information through various sensory channels can meet different user needs and contexts, creating expressions that can potentially improve the engagement by offering complementary or redundant information.

In the digitized world, different sensory modes have technically become the same at some level of representation, and they can be operated by one multi-skilled person, using one interface, one mode of physical manipulation, so that he or she can ask, at every point: "Shall I express this with sound or music?", "Shall I say this visually or verbally?"(Kress and van Leeuwen, 2001).

Sensory modalities such as auditory cues can effectively convey ambient information, direct attention and shape emotional tone, while the somatosensory system(the system responsible for our conscious awareness of touch, pressure, pain, temperature and body position(Purves et al., 2001).) offers a direct physical link to digital environments, enhancing feelings of presence and embodiment. 

Investigating how these multi-modal experiences can enhance immersion, evoke emotional responses, create richer and more embodied narrative contents, we aim to explore auditory and somatosensory capabilities when an environmental narration is introduced to an audience.
### Environmental as a Tool for Narration
*"The audience is not a passive observer, but actively investigates the frame both spatially and temporally, responding to the tension created within the narrative space(McErlean, 2018)"*

Given text from Interactive Narrative and Transmedia Storytelling highlights the new role and importance of the audience. Virtual spaces in interactive narratives are more than just digital settings. They are the environments where the story unfolds and where the audience actively participates. Environmental storytelling promotes virtual environments role from basic background to an active narrative agent. 

Strategically placed objects in the environment can tell a story on their own. A knocked-over chair, a specific book left open or a series of photographs can hint at past events, reveal aspects of a character's personality or provide clues that help the audience piece together the narrative(Dolinski, 2025).

In a professionally structured narrative there are macro and micro storytelling scopes. When it has done well, this hierarchy creates a depth of narrative design that neither approach could achieve alone, allowing the audience to connect grand macro and micro level events in ways that feel organic and profound(Dolinski, 2025). Environmental storytelling has the capability to convey stories that aren’t always directly told through dialogue or cutscenes.

Following example images from video games, movies and even from our real life, given to deepen understanding of environmental storytelling as a tool for narration;

![Figure 1](Images/environmental_storytelling_02.jpg)
**Figure 1.01:** An image from a public road.

On macro level scope, Figure 1.01 shows a shortcut made by people walking through the grass instead of using the sidewalk. The red-and-white barrier at the end of the path indicates an attempt to enforce the intended route, but the worn trail on the left shows people kept choosing the faster way.
![Figure 2](Images/environmental_storytelling_04.jpg)
**Figure 1.02:** A visual from a video game called Oblivion.

On micro level scope, Figure 1.02 tells a humorous story. A man lies exhausted beside a fiery figure on the floor next to a bed with a "Resist Fire" potion highlighted, hinting maybe he needed magical help to survive an intense, possibly romantic encounter.
![Figure 3](Images/environmental_storytelling_05.png)
**Figure 1.03:** An image of a building in Istanbul, Turkey.

With another macro level scope example, Figure 1.03 shows a building from Istanbul, made up of layers from different time periods, each added on top of the previous one. The labels on the right indicates the specific architectural style(starting with the Roman Empire at the bottom and ending with the Republic Era at the top) telling a visual story of Istanbul’s long and complex history. It reflects the city’s rich heritage, shaped by centuries of conflict, change and development, all embodied in a single structure.
![Figure 04](Images/environmental_storytelling_06.png)
**Figure 1.04:** A visual from a video game called Control.

With another micro level scope example, Figure 1.04 shows a character stands before a mail room door. The blood spreading under the door serves as an effective environmental narrative device, wordlessly hinting to the player the danger. Signalling that something violent has happened in the space they're about to enter, creating tension and anticipation without explicit exposition.

These examples provided to illustrate how this technique functions across various media and even in our physical world. What makes environmental storytelling special is that it lets each audience member piece together the story in their own way, creating a more personal connection.
### Personal Motivation
If I may be a bit more sincere and break the formal language of the last couple subchapters, I would like to start by introducing myself. 

Since I was a child I have been amused by video games and stories that have been told through video games. 

I remember the first time when I played a game called "SSX 3" which is a snowboarding game. I can still clearly recall the feeling when jumping off a cliff onto the snow surface and the simultaneous rumble coming from Dualshock 2(Figure 1.06). Feeling of the gritty snow texture when turning a tight corner or imminent hit response when I crashed into a barrier, as a child who was experiencing this kind of multi-modal experience for the first time, was really remarkable.
![Figure 1.05](Images/ssx3.jpg)
**Figure 1.05:** Video game SSX 3, PlayStation 2 (2003).

That memory of the Dualshock 2 rumbling in sync with the snowboarding action in SSX 3 really stuck with me. It wasn't just about seeing the snow or hearing the sounds; it was feeling the impact and the texture of that virtual world.

![Figure 1.06](Images/gamepad.jpeg)
**Figure 1.06:** Playstation 2 gamepad, Dualshock 2.

Dualshock 2 is the main physical user interface of the PlayStation 2, The vibration motors in the DualShock 2 were quite simple, basically small weights spinning off-center to create a general rumble. It was more of a strong shake or a light buzz(Tyson, retrieved 2025). Today, vibrotactile devices/tools are much more advanced, capable of producing a wider range of precise textures and feelings. Modern game controllers, like the Nintendo Switch's "HD Rumble" or the PlayStation 5's DualSense, can be an example in high definition haptic user interfaces. They can create much clearer and more varied tactile effects, like the subtle click of a dial, the tension of a bowstring, or the feeling of raindrops, making virtual interactions feel surprisingly realistic and nuanced.

![Figure 1.07](Images/vibration_motors_ds2.jpg)
**Figure 1.07:** Vibration motors of Dualshock 2.

My first hand experience and understanding that combining sound with touch could make a virtual experience feel incredibly real and immersive. With years of other experiences and knowledge about interaction and multi-modal stimuli, made me wonder how much more could be done if these sensory connections were designed intentionally to tell a story or convey specific feelings about an environment.

Embracing Sphere came to life as an idea with the background that I have stated. "Embracing Sphere", as a main title that on the one side, is poetic yet on the other side a direct analogy of user interaction for a playback system that will be briefly explained later. 

My artwork, therefore, aims to be a practical exploration of the ideas in this article. "Embracing Sphere" is designed to be a tool to investigate how these audio-tactile experiences can shape our perception of a virtual space, its materials, and the subtle narrative cues embedded within it. It’s my way of testing how powerful this multi-modality of hearing and touch can be in making environmental storytelling more engaging for an audience.
### Room Acoustics
*"Sound is something most people take for granted. Our environment is full of noises, which we have been exposed to from before birth. What is sound, how does it propagate and how can it be quantified(Howard & Angus, 1996)?"* 

The purpose of this subchapter is to introduce fundamental knowledge ground for room acoustics and describe the usage of room impulse responses in the Embracing Sphere context.

Sound is simply a mechanical disturbance of the medium. Medium in that context may be air, solid, liquid or other gas matters. Dependent on the mediums state, the sound can be propagated and while this propagation happens it interacts with physical objects and other sound waves. In room acoustics the interactions of the sound with the medium, basically can be listed as refraction, absorption, reflection and interference. Psychoacoustics is the study how humans perceive sound after all these interactions with the medium(Howard & Angus, 1996). 

The heard sound, is the result of all these complex physical interactions in the place our ears are located. 

When sound moves through a room, its behavior is shaped by how it interacts with surfaces, mainly through absorption and reflection. Sound reflection occurs when sound waves hit a hard boundary and bounce back into space. In contrast, sound absorption is when a material takes in the sound's energy, which is converted into small amounts of heat through internal friction, reducing the amount of sound that reflects(Howard & Angus, 1996). For example, a wooden surface absorbs more sound than a rough concrete one. These interactions, along with others like refraction and interference, collectively determine the acoustic character of a room.

These interactions do not occur in isolation. They collectively define the complex behavior of sound waves and their propagation within the room. Each time the sound interacts with a surface in the room it loses some of its energy due to absorption and reflection. The time that it takes for sound at a given time to die away in a room is called the reverberation time.

Reverberation time is an important aspect of sound behavior in a room. Mentioned different absorption coefficient values in different materials and frequencies shapes the perception of the room. If the sound dies away very quickly, we perceive the room as being “dead” or if the sound dies away very slowly, we perceive the room as being “live”. To calculate reverberation times there is a simple formula known as the “Sabine formula,” named after its developer Wallace Clement Sabine(Howard & Angus, 1996). 
$$T_{60} = \frac{0.161 \cdot V}{A}$$
- T60: This is the reverberation time in seconds. It's defined as the time it takes for the sound pressure level in a room to decrease by 60 decibels (dB) after the sound source has stopped.
- 0.161: This is a constant. Its units are seconds per meter (s/m). This constant is derived empirically and is based on the speed of sound in air at a typical room temperature.
- V: This represents the volume of the room in cubic meters. Calculated by multiplying the length, width, and height of the room.
- A: This is the total sound absorption of the room in Sabins. It's calculated by summing the absorption of all surfaces in the room. The absorption of each surface is found by multiplying its surface area in square meters by its sound absorption coefficient at a specific frequency.

According to the Sabine formula, reverberation time depends on the volume, surface area, and the average absorption coefficient in the room. However, the absorption coefficients of real materials are not constant with frequency. This difference in absorption strength in different frequencies changes heard timbre of the room as the sound in the room decays away. Apart from being useful, Sabine formula has assumptions for speed of sound and static response of the reflective materials in the room. To more accurately measure reverberation time, another method introduced in 1964 by M. R. Schroeder called room impulse response capturing(Schroeder, 1964).

The method uses tone bursts (or filtered pistol shots) to excite the enclosure(room). The captured smooth decay curves resulting from the new method improve the accuracy of reverberation time measurements and facilitate the detection of non-exponential decays(Schroeder, 1964).

These impulse response recordings later can be used to reconstruct a virtual environment with the same reverberation curves as captured room with a mathematical operation called convolution. An anechoic(no reflections) sound is convolved with an RIR and this mathematical process applies the room's acoustic snapshot to the sound. The convolution effectively embeds the reflections and reverberation captured in the RIR to the original sound.

After a long physics and mathematics explanation there is a need to collect all given knowledge and link with the Embracing Sphere.
#### Sonic Perception and Interpretation in Environment

"My impaired senses mean that I can’t take in the world around me directly. I think this is why my mind turned more and more to abstract thought. I had to learn to estimate how far away an object is using my mind. At every step. And this way, I got into the habit of abstract thought in other areas as well.(Iannis Xenakis)"

The impact of acoustic environments on human perception was a concept explored by architect and composer Iannis Xenakis. His experiences, such as severe injuries he sustained during World War II which affected his hearing and vision and intensified his senses to the sonic aspects of space. This relation is one of the leading drivers of my inspirations for using room simulations to convey an auditory environmental story. 

Hearing covers a big part in our sensory system to understand and interpret the environment that surrounds us. Sonic environments deliberately need acoustics and psychoacoustics knowledge to give more colors in the palette of a painter. 

Deriving from the view that we've stated, a procedural room impulse response program developed to use in Embracing Sphere. Procedural Room Impulse Response Generator will be investigated more in the proceeding chapter "Conceptual Framework, Software Programs".
### Haptics
The somatic system can be subdivided into three elements: kinesthetic, visceral, and cutaneous. Kinesthetic sensation uses signals from proprioceptors in the joints, muscles, and tendons to provide feedback to the brain on the position and forces within segments. Similarly, visceral sensation uses receptors in the abdomen. Cutaneous sensation consists of a combined response of four types of nerve endings in the skin(Mansfield, 2005). The haptic system uses sensory information derived from mechanoreceptors embedded in the skin, muscles, tendons and joints(Lederman, 2009).

Haptic interaction can be stimulated by different devices but such as thermal feedback and electro-vibration are outside the scope of this study thus a vibrotactile device chosen for this research purpose. These vibrotactile devices are similar to those of loudspeakers and voice coil actuators(Remache-Vinueza et al., 2021), allowing for conventional audio recording practices viable on haptic feedback content creation.

![Figure 1.08](Images/vibrotactile_bass-shaker.jpg)
**Figure 1.08:** Voice coil actuator, vibrotactile device, Dayton Audio BST-1.

The sensory system is a network that enables your body to receive information from the environment and its own internal state, converting stimuli into signals for the brain to process. Human sensory system doesn't just process this sensory information as a single stream; it organizes it to answer fundamental questions about the environment(Reed et al,. 2005). Research in sensory neuroscience suggests a fundamental distinction in how the brain processes sensory information framed as "what" an object(disturbance) is versus "where" it is located.

How do you feel the difference between rough stone, resonant wood, or soft earth? This relates directly to identifying the "what" of the surrounding environment. The "where" pathway provides spatial information, helping us understand the location of a stimulus in relation to our body and within the environment. The location of a distant explosion felt through the floor, or the feeling of being in a small, enclosed space versus an open one? This is related to identifying "where" information.

Within the study that explores environmental storytelling through audio-tactile stimulation, we can extend this framework with a third component, "how". This component can include "cause and effect" relation into our sensory perception and cognition. Where "what" and "where" components answer material and spatial questions, "how" components can answer temporal questions derived from the first two components. Focusing on a more interactive concept of "event" rather than a static stimulation characteristics.

This "what, where and how" taxonomy provides a conceptual tool for environmental storytelling, thus embedding temporal relations into the environment, moving beyond simple rumbles to convey specific information about an environment's materials, spatial layouts and past/ongoing events.
![Figure 1.09](Images/rumble_strips.jpg)
**Figure 1.09:** A visual shows road rumble strips.

As shown in the Figure 1.09 rumble strips designed to alert drivers by creating vibrations and noise when a vehicle goes out from its intended lane or crosses the edge of the road. Stimulation from a rumble strip side of the road not just indicating physical position or a road surface information, it's an immediate warning. 

The sensation isn't a random patch of bad road; it's a deliberately engineered, rhythmic pattern. This pattern connects the what (the ribbed texture) and the where (the edge of the lane) to create a temporal meaning: "You are currently in the process of making a mistake." The "how" pathway interprets this sequence as a cause-and-effect event, because you are drifting, you are feeling this vibration. In a structured narrative context, this type of haptic stimulation can be utilized for environmental storytelling.## Conceptual Framework
### Hardware Devices
### Software Programs
## Future Works
## Conclusion
## References
1. Dolinski, B. (n.d.). _Environmental storytelling in video games_. Game Design Skills. Retrieved June 3, 2025, from https://gamedesignskills.com/game-design/environmental-storytelling/
2. Cachón-Ramón, D., Pozo-AUñón, R. A., & Prados-Peña, M. B. (2023). Unravelling the complexity of the Video Game Industry: An integrative framework and future research directions. _Telematics and Informatics Reports_, _12_, 100100.
3. Kress, G., van Leeuwen, T. (2001). _Multimodal Discourse: The Modes and Media of Contemporary Communication_. New York: Oxford University Press.
4. Purves D., Augustine G.J., Fitzpatrick D., et al., editors. Neuroscience. 2nd edition. Sunderland (MA): Sinauer Associates; 2001. Chapter 9, The Somatic Sensory System.
5. McErlean, K. (2018). Interactive Narratives and Transmedia Storytelling: Creating Immersive Stories Across New Media Platforms (1st ed.). Routledge.
6. Tyson, J., _How PlayStation 2 works_. HowStuffWorks. Retrieved June 3, 2025, from https://electronics.howstuffworks.com/ps23.htm
7. S. J. Lederman and R. L. Klatzky, “Haptic Perception: A Tutorial,” Attention, Perception, & Psychophysics, vol. 71, no. 7, pp. 1439–1459, 2009.
8. Remache-Vinueza, B., Trujillo-León, A., Zapata, M., Sarmiento-Ortiz, F., & Vidal-Verdú, F. (2021). Audio-Tactile Rendering: A Review on Technology and Methods to Convey Musical Information through the Sense of Touch. _Sensors_, _21_(19), 6575.
9. Howard, D., Angus, J., (1996). Acoustics and Psychoacoustics, Focal Press
10. Acoustic Traffic, Retrieved June 3, 2025, from https://www.acoustic.ua/st/web_absorption_data_eng.pdf
11. Schroeder, M. R. (1965). New method of measuring reverberation time. _The Journal of the Acoustical Society of America, 37_(3), 409–412.
12. Fastner, C. (n.d.). _Iannis xenakis: Architect of sound_. Elbphilharmonie Mediatheque. https://www.elbphilharmonie.de/en/mediatheque/iannis-xenakis-architect-of-sound/287
13. Reed, C. L., Klatzky, R. L., & Halgren, E. (2005). What vs. where in touch: An fMRI study. _NeuroImage, 25_(3), 718–726.
14. Creem, S. H., & Proffitt, D. R. (2001). Defining the cortical visual systems: "What", "Where", and "How". _Acta Psychologica, 107_(1–3), 43–68.
15. Mansfield, N. J., (2005). Human Response to Vibration, CRC Press