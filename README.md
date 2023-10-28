# 471-Project-1

This project was completed by Lauren Garvey.

In this repository is a program that implements noise gating, flanging, and TK effects to a drum synthesizer component, built on top of the Synthie program provided by the CSE 471 professors at MSU. Also included are audio files demonstrating the effects and the synthesizer. Finally, there is a piece showing off all of the components working together.

First, here is the main piece, titled TK title:

TK main song

Included in this repository with the filename 'TK title.score' is the XML file detailing the score used for this selection. As shown in that file, the scores used for this program are in XML format, and are broken up by instruments - this can be a ToneInstrument, a drum synthesizer instrument, or one of the effects. Each of the effects then further specify their unique information within a 'note' tag in the XML - for example, the flanging effect specifies a maximum delay, frequency, and buffer size for its implementation. For this project, I implemented a drum synthesizer component, which can play any of a bass, snare, two toms, and cymbals. The XML for these is specified as 'BassDrum', 'SnareDrum', 'LeftTom', 'RightTom', and 'Cymbals'.

Next, here is a piece demonstrating the three effects:

TK effects piece

The score for this piece is included in this repository under the name 'TK effects.score".

Finally, here is a piece demonstrating the drum synthesizer component:

TK synth piece

The score for this piece is included in this repository under the name 'TK synth.score".
