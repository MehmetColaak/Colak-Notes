## Title
****
### Embracing Sphere: Auditory Environmental Narration with Audio-Tactile Playback Systems

## Structure
#### 1 Introduction
1.1 Research Question: How multi-modal stimulation can be utilized to enhance auditory environmental narration?
1.2 Multi-Modality: How does the integration of audio and tactile feedback influence the perception and interpretation of environmental narratives in an interactive art context?
1.3 Environment as a Tool for Narration: State clearly what your project sets out to achieve (e.g., "To design, implement, and evaluate an interactive audio-tactile system capable of procedurally generating environmental snapshots for narrative purposes").
1.4 Embracing Sphere and My Own Perception: Briefly outline the novelty of your work (e.g., the specific procedural generation method, the integration approach, the application to narrative via an art installation).
1.5 Scope and Limitations: Define the boundaries of your research (e.g., types of environments modeled, specific haptic modalities used, complexity of the narrative, scale of the user evaluation if any).
1.6 Thesis Outline: Briefly state what each subsequent chapter will cover.

#### 2 Background and Related Works in the Field
2.1 Environmental Narration
	2.1.1 Definition: Define "environmental narration" (storytelling through space, atmosphere, implicit cues).
	2.1.2 Existing Methods in Different Mediums: Discuss existing techniques in games, film, sound art, and literature (e.g., sound design, level design, environmental puzzles, use of acoustics).
	2.1.3 Auditory Environmental Narration: Give an example from the Game Return of the Obra Dinn. 
2.2 Room Acoustics
	2.2.1 Definition: Explain Room Impulse Responses (RIRs): what they are, what information they contain (reverberation, spatial cues).
	2.2.2 Room Impulse Response Measurement Methods: Overview of RIR measurement techniques.
	2.2.3 Convolution in Math and Digital Audio: Explain Convolution operation and usage in audio-visual content.
	2.2.4 Room Acoustics in Sound Art: Explain Alvin Lucier - "I Am Sitting in a Room" Process-based art, using the room's acoustics as both medium _and_ subject, the iterative feedback loop revealing resonant frequencies.
2.3 Procedural Audio Generation
	2.3.1 Procedural Content in Video Games: Define procedural content generation and give examples from games and interactive applications.
	2.3.2 Procedural Audio and Synthesis: Explain methods of generating audio procedurally.
	2.3.3 Integrating Procedural Generation into RIR: Introduce a method for generating RIR's procedurally.
2.4 Haptics and Perception
	2.4.1 Overview of Haptics: Explain different haptic feedback modalities (vibrotactile, force feedback, etc.) relevant to your project.
	2.4.2 Human Tactile Perception: Briefly cover human tactile perception (how we sense texture, vibration, impact).
	2.4.3 Usage: Examples of haptics in HCI, VR/AR, accessibility, and gaming.
2.5 Audio-Tactile Interaction
	2.5.1 Definition: Define audio-tactility and explain differences from other multi-modal systems.
	2.5.2 Usage of Audio-Tactility in Media: Examples of systems or experiences integrating audio and haptics.
#### 3 System Design and Methodology
3.1 Conceptual Framework: Explain how user interaction, procedural generation, audio rendering, haptic rendering, and narrative elements connect in your system.
3.2 Procedural RIR Generation System: Detail the algorithms/methods used to generate RIRs (acoustic snapshots). What parameters influence them (e.g., simulated room dimensions, material properties, source/listener position)?
3.3 Audio Playback System: How are the RIRs applied (e.g., real-time convolution)? What audio engine/libraries are used? Output format (stereo, binaural, ambisonics)?
3.4 Haptic Playback System: Describe the haptic hardware (actuators, placement, controllers). 
3.5 Interaction Design: How does the user interact? What actions trigger the generation/playback? How is the narrative progression linked to interaction?
3.6 Narrative Structure: Explain how the environmental snapshots are used to convey the intended narrative.
#### 4 Implementation
4.1 Hardware Setup: Detailed description of the physical components used (computer, audio interface, specific speakers/headphones, specific haptic devices, sensors, etc.) and how they are connected. Include diagrams/photos if helpful.
4.2 Software Development: Languages, frameworks, libraries (e.g., Max/MSP, Pure Data, C++, Python, Unity, Wwise, custom code) used for the procedural engine, audio/haptic rendering, and interaction logic.
4.3 Art Project Realization: Describe the physical form and user experience of your interactive art installation.
4.4 Challenges and Solutions: Discuss key technical hurdles encountered during implementation and how you overcame them.

#### 5 Evaluation
5.1 Evaluation Goals: What aspects of the system are you evaluating (e.g., technical performance, effectiveness of conveying space/material, narrative impact, user engagement)?
5.2 Methodology: Describe your evaluation approach. Examples:
	5.2.1 Perceptual Effectiveness: Can participants understand environmental changes or narrative shifts based on haptic/audio-only cues?
    5.2.2 Narrative Comprehension: Participants reconstructing narrative from stimulus to see how well the system conveys narrative arcs without visuals.
    5.2.3 Qualitative Analysis: Interviews/focus groups analyzing richness, imaginative engagement, or associations evoked.
    5.2.4 Technical Performance: Latency between tactile/audio triggers, fidelity of convolution reverb simulation, procedural realism of RIRs.
5.3 Results: Present the collected data (quantitative and/or qualitative).
5.4 Discussion: Interpret the results in relation to your research questions and goals. What worked well? What were the limitations? How did users respond to the audio-tactile combination?
#### 6 Conclusion
6.1 Summary of Findings: Briefly reiterate the main achievements and findings of your project.
6.2 Answering Research Questions: Explicitly address the research questions posed in the introduction based on your work.
6.3 Contribution Revisited: Restate the significance and novelty of your work in light of the results.
6.4 Limitations: Honestly discuss the limitations of your system, implementation, and evaluation.
## Keywords
- Environmental Snapshots
- Audio-Tactile
- Auditory Environmental Narration