### Keywords
	User Interface, Haptics, Audio, Multimodal, Latency, Synchronization
### Introduction
When two objects collide, we have a contact interaction. These contact interactions can produce characteristic sounds and forces that communicate information about our relationship with rigid objects and the surrounding environment.

They are introducing and interface called AHI and it is user interaction device with the simulated environment generates contact forces. 
### Audio Force Synthesis
Naively using the raw normal forces to synthesize audio produces unsatisfying results.
Waiting 10ms before decaying improves the quality of impulsive contacts, whereas decaying the audio force immediately upon contact excessively reduces the overall amplitude and dynamic range of the resulting audio signal.
### Real-Time Simulation
The basic control structure for the AHI real-time synthesis and simulation is interrupt-driven. There is a haptic interrupt service routine (HISR) that generates haptic and audio forces and an audio interrupt service routine (AISR) that convolves the audio force with the impulse response of the modelled object. Using these two separate interrupts we can synthesize the audio signal at a much higher rate than we generate haptic feedback.
### Conclusion
Designing compelling simulated environments is the high-level goal of this research. The representation and rendering of contact interactions comprises an essential component of any such simulation. Atomically representing the contact event as something that produces both sound and force helps integrate auditory and haptic stimuli. We believe this is a natural way to think of representing and simulating contact. We have implemented a new interface that can render audio and haptic interaction atomically.