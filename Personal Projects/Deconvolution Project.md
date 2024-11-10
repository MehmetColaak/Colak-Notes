Deconvolution Project is an simple audio tool to create room impulse responses. 

This script calculates the deconvolution of audio signals to extract the impulse response from a recorded audio file using a reference file. It uses the `librosa`, `numpy`, `soundfile`, `matplotlib` and `scipy` libraries for signal processing and the `tkinter` library for file dialogues.

In future iterations I want to create an audiovisual work with it. It may contain:
- An analogy of snapshotting the acoustic space
- Exploration of a representation of the IR time series in different mediums like qr, barcode etc.
- Combined presentation of two different sensation(visual and aural snapshot of an acoustic space)

While exploring and curating acoustic spaces there has to be some qualifications to categorize and differentiate spaces and and their acoustic snapshots. So these are my main lookups for acoustic characteristics:
- RT60 curve
- General sound propagation
- Early reflections
- Color of the reverb tail
- Specific room acoustic events that creates artifacts or standing waves

Another iteration from the foundation of this project is mining snapshots from audio processing tools like fx plugins(reverbs, filters, delays, flangers, phasors etc.). With this approach rerecording a reference track through a certain fx plugin or a chain and using deconvolution for extracting impulse response, you can create audio time series from that exact fx plugins.

