# 471-Project-1

This project was completed by Lauren Garvey. ChatGPT was used for determining the basic structure of generating waveform tables.

In this repository is a program that implements noise gating, flanging, and compression effects to a drum synthesizer component, built on top of the Synthie program provided by the CSE 471 professors at MSU. Also included are audio files with their corresponding .score files that demonstrate the effects and the synthesizer. Finally, there is a piece showing off all of the components working together.

## Score file format

When generating the audio files, the program uses XML score files titled in the format "title.score". Each score file starts by identifying itself as an XML file, with the corresponding version and UTF encoding. Next is the 'score' tag, which specifies the beats per minute ('bpm') and the beats per measure. Nested in the score tag are the instrument tags, which can be specified as BassDrum, SnareDrum, LeftTom, RightTom, Cymbals, ToneInstrument, NoiseGate, Flanging, or Compression. All of these instrument tags then specify their own notes, which tell the program when and how that instrument should play. Common to every instrument are the measure when the note should be played ('measure'), the beat in that measure to play on ('beat'), how long to play that note ('duration'), and the note itself ('note').

The last three listed instruments are effects components:

- Flanging mixes two signals and delays one by a small and changing period. Its note tags additionally specify the maximum delay a signal can be ('delay'), the frequency at which the signal should modulate ('frequency'), and how many signals should be stored and repeated ('buffersize').
- Noise gating stops sounds below a specified threshold from playing. Its note tags additionally specify the minimum frequency a signal must reach in order for the program to play its audio ('threshold'), the fade-in duration from silence to playing a given note ('attack'), and the fade-out duration from playing a given note to silence ('release').
- Compression applies compression and limiting, reducing the volume of sounds above a certain threshold. Its note tags additionally specify the maximum frequency a signal can reach before being reduced ('threshold'), how much that signal should be reduced ('compressionratio'), and a limit to apply to the peaks that prevents the signal from getting clipped or distorted ('limit').

The first five listed are various drum synthesizer components. Common to all five are characteristics for envelope generation, which details how the note should begin and end. These characteristics are how long it should take for the sound to reach peak amplitude ('attack'), how long it should take for the sound to decay to its sustaining level ('decaytime'), the volume level during the sustaining phase ('sustainlevel'), how long it should take for the sound to fade out after releasing ('release'), and the overall volume of the sound ('amplitude').

## Music pieces

First, here is the main piece, titled TK title:

TK main song

Included in this repository with the filename 'TK title.score' is the XML file detailing the score used for this selection. As shown in that file, the scores used for this program are in XML format, and are broken up by instruments - this can be a ToneInstrument, a drum synthesizer instrument, or one of the effects. Each of the effects then further specify their unique information within a 'note' tag in the XML - for example, the flanging effect specifies a maximum delay, frequency, and buffer size for its implementation. For this project, I implemented a drum synthesizer component, which can play any of a bass, snare, two toms, and cymbals. The XML for these is specified as 'BassDrum', 'SnareDrum', 'LeftTom', 'RightTom', and 'Cymbals'.

Next, here is a piece demonstrating the three effects:

TK effects piece

The score for this piece is included in this repository under the name 'TK effects.score".

Finally, here is a piece demonstrating the drum synthesizer component:

TK synth piece

The score for this piece is included in this repository under the name 'TK synth.score".
