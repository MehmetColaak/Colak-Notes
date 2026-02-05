# 1. Cover Page
Embracing Sphere: an Environmental Storytelling with Audio-Tactile Playback System
Mehmet Çolak
Interface Cultures Master's Thesis Defense
# 2. List of Content
- What is Embracing Sphere
- Why, How?
- Research Questions
- Sub-Categories of Embracing Sphere
- Environmental Storytelling
- Environmental Storytelling Examples in Media
- Audio-Tactile Representation of an Environment
- Space and Acoustics in Artistic/Scientific Perspective
- Acoustic Measurement Techniques and Artistic Examples
- My Approach
- Haptics
- Vibrotactile Devices and Video Game Industry
- Ars Electronica Festival
- Embracing Sphere System Design, Methodology and Implementation
- Content Creation for the Medium
- Storyboard
- Vibrotactile Content
- Auditory Content
- Observations from Ars Electronica Festival
- Future of Embracing Sphere
# 3. What is Embracing Sphere
An interactive audio-tactile interface and artwork investigating how multi-modal environmental storytelling can be conveyed through non-visual mediums.
# 4. Why, How?
**Why:** Inspired by early experiences with multimodal feedback in video games, like the DualShock 2 controller, which made the virtual world feel tangible and real.

**How:** By creating a multi-modal experience using simultaneous audio playback—which incorporates procedurally generated Room Impulse Responses (RIRs), and synchronized vibrotactile feedback from bass shakers.
# 5. Research Questions
1. To what extent does multi-modality play a role in the environmental storytelling?
2. How multi-modal stimulation can be utilized to enhance auditory environmental storytelling?
3. How effectively can an interactive audio-tactile system convey environmental characteristics and narrative cues?
# 6. Sub-Categories of Embracing Sphere
- Environmental Storytelling
- Acoustics
- Haptics
# 7. Environmental Storytelling
The story element is infused into the physical space, where the environment becomes a silent narrator communicating through carefully crafted details that enhance immersion.

Unlike traditional storytelling methods that rely on delivering a story through dialogue, cutscenes or text dumps; environmental storytelling operates more subtly.

It exists in a unique space between a pre-authored "embedded narrative" and a player-driven "emergent narrative".
# 8. Environmental Storytelling Examples in Media
- Visuals
- Journey: Tells its story entirely through movement and exploration, using the environment and diegetic feedback to guide the narrative.
- Return of the Obra Dinn: A prime example of auditory environmental storytelling, where audio snippets from the past are used to solve a mystery.
# 9. Audio-Tactile Representation of an Environment
Combining distinct modalities like audio and acoustic simulations for space, and tactile pulses for texture and tactile hints, offers a novel way to represent an environment.
# 10. Space and Acoustics in Artistic/Scientific Perspective
# 11. Acoustic Measurement Techniques and Artistic Examples
- Room Impulse Response (RIR): An "acoustic snapshot" of a space, capturing its unique reverberation characteristics. RIRs can be measured using techniques like popping a balloon or, more accurately, the sine sweep method.
- Convolution: The mathematical process of applying an RIR to a dry audio signal, effectively placing the sound within that virtual space.
- Artistic Example: Alvin Lucier's _I am sitting in a room_, where the room's own resonant frequencies become the musical content, turning the space into an instrument.
# 12. My Approach
EXAMPLE: Nine Inch Nails - Copy of a
- Instead of using pre-recorded RIRs, Embracing Sphere uses procedural generation to create them in real-time.
- The system uses the Sabine formula with randomized room dimensions and absorption values to generate unique acoustic spaces on the fly.
- This aleatoric approach allows for dynamic and varied environmental shifts within the narrative.
# 13. Haptics
- A "what, where, and how" design taxonomy was used to create haptic feedback that conveys material properties (what), spatial location (where), and events (how).
- This is achieved with **Voice Coil Actuators (VCAs)**, which function like small speakers and allow for detailed haptic design using standard audio tools.
- For Embracing Sphere, I intentionally chose the auditory and haptic modalities to use the ability to create contrasts and harmonies within the same scenery.
- Spatio-temporal narration can be done with many different sensory modalities, but auditory and somatic senses fundamentally need a temporal ground to be perceived and have capabilities for conveying spatial cues[56].
EXAMPLE: Road Rumble Strips.
# 14. Vibrotactile Devices and Video Game Industry
- Racing Simulators: Games like iRacing use detailed vehicle telemetry to provide realistic force feedback, allowing players to feel the road texture, tire grip, and weight transfer, which dramatically increases immersion, and enhances interaction performance.
EXAMPLE: Astro's World, Dualsense Videos
# 15. Ars Electronica Festival
Embracing Sphere exhibited at the Ars Electronica Festival 2025 as part of the Interface Cultures, Campus Exhibition.
# 16. Embracing Sphere System Design, Methodology and Implementation
**Hardware Setup:**
- A car seat mounted on a sim-racing frame forms the physical interface.
- Powered by a **Raspberry Pi 5**, with an **ESI GigaPort EX** sound card for multi-channel output.
- Three Dayton Audio BST-1 bass shakers provide vibrotactile feedback, driven by a power amplifier.
- A  sensor automatically starts the experience when a user is seated.
**Software Development:**
- Reaper (DAW) was used for sound design and authoring the audio and haptic layers.
- Pure Data was used to manage the interactive playback logic and the procedural generation of RIRs.
# 17. Content Creation for the Medium: The Story
- A narrative was designed specifically for the audio-tactile experience.
- The narrative follows a car journey that transitions into drowning and flashback sequences, exploring themes of panic and acceptance. The car environment was chosen as it is a powerful real-world example of multimodal presence as transportation.
- Vibrotactile Content: Created by sampling real-world vibrations such as the Neue Eisenbahnbrücke in Linz and reverse-engineering haptic feedback from racing simulations.
- Auditory Content: A 3D ambisonic audio mix was created and delivered via headphones. Procedurally generated RIRs were used to give flash-memory sequences a distinct acoustic feeling.
# 18. Observations from Ars Electronica Festival
Negative Feedbacks and Observations:
- The low seated racing seat was physically challenging for some visitors to get in and out of.
- A two-second silence in the storyline was frequently misinterpreted as the end of the experience, causing users to leave prematurely.
Positive Feedbacks and Observations:
- Many visitors reported feeling genuinely transported, asking, "It felt like I was in a car. How did you do it?". 
- Visitors were eager to understand how the audio-tactile effects were achieved. Curiosity about technical accomplishments behind the seat was remarkable.
# 19. Future of the Embracing Sphere
- Improve Ergonomics & Spatial Audio: Redesign seating for better accessibility and enhance RIR generation with early reflections for clearer space perception.
- Expand Content Library: Create diverse audio-tactile environmental snapshots beyond car journeys.
- Add User Interactivity: Implement real-time controls for scenario navigation and personalized haptic intensity adjustment.
- Conduct Formal Evaluation: Perform structured user studies with questionnaires and physiological measurements to validate storytelling effectiveness.
# 20. Thanks
- Thanks
- Q&A