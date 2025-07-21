The Embracing Sphere installation is built into a physical car seat. When a user is seated, the system plays a pre-authored experience composed of synchronized audio and vibrotactile events. The following subsections detail the hardware and software components that sets the installation.
### Hardware Setup
As main processing unit of the playback system, a microcontroller Raspberry Pi 5 has chosen. Raspberry Pi is a small processing unit that can run traditional personal computer operating systems such as Linux. This small computer has chosen for its small form factor and GPIO pin usage. 

Playback system is interactive according to audience behavior with limits and some sensors required to use as a detection point. In that case a light sensor used to detect if any user is seated or not. If a user is seated, idling loop stops and main experience initiates.

The audio channels that drives headphones requires 2 channels to play binaural audio which isolates the listener within the sonic environment and another 3 channels required to drive voice coil actuators. 

In total at least 5 channels needed to create this playback system that drives both auditory and vibrotactile parts of the installation. For 5 independent channels of audio output, ESI GigaPort EX sound device has chosen. Sound devices are hardwares used in recording and monitoring efficiently through ADDA (analog to digital, digital to analog) converters\cite{}. This sound device has 8 individual audio outputs and it is class compliant, available to use in linux systems like Raspberry Pi 5.

These 8 analog outputs are line level -10 dBV RCA outputs which is enough to drive headphones but lack of power to drive bass shakers that needs 50W of energy to work. To amplify the haptic channels, Thomann t.amp S-100 MKII power amplifier selected.

Mounting VCA's into the seat and connecting cables into sound device then processing unit  very was intuitive. A sim-racing metal frame used for fixing everything into the seat. Metal frame also helped on transmission of vibrations through the chasis, it elevated whole body vibration feeling.

Hardware setup and tests such as sine and noise signals and transient signals for testing lag between headphone and the actuators has done. After setting up the signal flow, a stress test has made where every actuators tested in loudest state without clipping in any part of the system. I was quite impressed by the results of the first tests. Overall loudness was alright and vibrotactile feeling was really distinctive. 
## Software Development
After assembling every instrument together software development and practicing actual sound design started. The Embracing Sphere includes fixed media in the main content (fixed time and event sequences) and procedural effect chain. Therefore I utilized a Digital Audio Workstation (DAW) called Reaper, for sound design and authoring of the sound design. To achieve user interaction and procedural effect chain I used Pure Data, a visual scripting software for interactive audio-visual projects.

In Reaper, I have structured a hierarchy in the sound layers of the experience. In that structure audio signals and vibrotactile signals are separated into 2 different effect chains. Audio signals/events in the audio channels first spatialized with the IEM Suite plugins (Institute of Electronic Music), an ambisonic plugin toolkit that has utilities for spatial encoding and decoding, then decoded for binaural monitoring and that monitored output exported to use in the Pure Data patch.

Vibrotactile signal just filtered with low pass filter, a filter that filters audio signal above certain frequencies. This filtering was necessary to display audio signals with the bass shakers, as mentioned before, bass shakers have a ceiling on frequency to displayed, any signal that has frequency content above 80Hz creating unwanted artifacts and issues on the bass shaker.

IMAGE

After sound design process finished, a test patch created on Pure Data. This patch allows to simulate exhibition environment by changing play states on mouse click. Image of the patch can be seen in the figure \ref{} below.

IMAGE

Further developments on the patch includes translating procedural RIR patch from Max/MSP to Pure Data and setting the patch as startup command in the Raspberry Pi 5 to ensure seamless integration of the artwork in the exhibition.

The command made by editing autostart file in the Raspberry Pi 5 by adding a line shown below.

This specific command starts the patch on startup with given instructions such as "-nogui" which is directing no graphic user interface while playing and some audio playback format instructions for our audio content.
## Challenges and Solutions
One of the biggest challenges I have seen while I was developing Embracing Sphere, finding  good sources for vibrotactile content creation. Despite many written and video sources available for sound design and audio content creation, vibrotactile content creation tutorials or fundamental knowledge were not enough in comparison with audio domain.

I have solved this issue with reverse engineering already established interactive applications such as video games and racing simulations. By sampling these applications I had a chance to examine vibrotactile content of these interactive applications. Some samples I recorded are used in Embracing Sphere's vibrotactile later such as tire and engine rumble of the vehicle.

IMAGE

Another challenge I've faced is trial and error pattern was rather slower than desired. To solve this challenge I chose same approach with Emoti-Chair project \cite{}. I used the seat itself to author the audio and vibrotactile content, I sat on the seat while editing and designing, monitored the overall feeling immediately. This approach reminded me theater mixing in cinema industry, tailored content is directly displayed, evaluated in the corresponding display system.

IMAGE

In design and storyboard preparations, I've faced a challenge of finding right multi-modal sensory scenarios to successfully create an environmental storytelling. After a long thinking about real-life experiences that affected me directly with auditory and tactile modalities, I came up with an idea of story that happens mostly inside a car. This decision is derived from both my own experiences and a research about presence, "At the Heart of It All: The Concept of Presence"\cite{}. According to this research about presence, the experience of being inside a moving vehicle represents a perfect example of "presence as transportation" where multiple sensory modalities work in harmony to create the illusion of moving through space while remaining physically stationary relative to the vehicle interior.

The research shows that presence works best when visual, audio and tactile feedback combined together. Vibrotactile modality highlighted important especially for creating realistic environmental experiences. This multi-modal approach aligns perfectly with the aims of Embracing Sphere, as the car environment naturally provides rich opportunities for meaningful vibrotactile content such as the subtle rumble of the engine transmitted through the seat to the varying textures of different road surfaces felt through the vehicle chassis.

Secondly, from my own experiences I think that creating contrast situations and implementing these two distinctive situations, enhances both end of the spectrum such as a subtle vibrating bridge to saturated stimulations of being inside of a car that is falling into the sea.

Embedding environmental storytelling cues in this story was the biggest challenge I've faced. Because of short length of the story I placed short term environmental cues such as, rumble strips on the road and semi-open window next to passenger seat ends up being catastrophic results. For more long term environmental cues I used more abstract approach by using procedural RIR to enhance flash memory sequences more vibrant and distinctive.

Ensuring the user-experience will be the same as my intentions within the story was hardest but this is the challenge of many creative practices. For now I cling onto believing in my creative craft.