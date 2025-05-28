# Frontend-Audio-Plugin
Introduction: 


Team Members for full OneSend3D Project:
● Kelvin Peterson:
  ○ Frontend developer/Researcher
  ○ kelvin_peterson@wheatoncollege.edu
  ○ pdkelvin11@gmail.com
  
● Connor White:
  ○ Backend developer/Researcher
  ○ white_connor@wheatoncollege.edu
  ○ connoriferous@gmail.com


How to Run and Sample Input/Output:
I personally ran the code in visual studio by opening the folder that contains the CombineBoth.sln and then selecting that solution. Then the source code will be displayed and what you will do is at the top click the build button and then click the build solution button. After it is done building righht below the build there is another one on the screen that give you the option to either set the built solution to either release or debug (pick either one), and then one you select the you will then press the filled in green play button to actually run all the code.
![Screenshot 2025-05-28 104508](https://github.com/user-attachments/assets/857d0bf7-3d5f-4b44-955e-459859ae0904)

This is what the UI will look like when you first run the code successfully (This is an example with some audio playing). 
![Screenshot 2025-05-09 224454](https://github.com/user-attachments/assets/0a0f6549-44bc-455e-affe-2b8a5b54b464)

Description of what the sliders do are below.

If you click either Load Audio and select the audio you want to be played or start playing and midi keyboard or start speaking, it will look something like this (will vary based on audio).

The output is produced visually in the Spectrum Analyzer which is the big graph at the top of the screen.

Troubleshooting:
Make sure that all the code has access to every file in both folders. If using visual studio, click the project button at the top of the screen inside visual studio, click CombineBoth_SharedCode Properties, change the configuration to release and then click C/C++ tab. Once you are there click the Additional Include Directories, then the down arrow and edit. Finally add the address of the folders inside of the Combineboth.zip folder you have downloaded. Once you click ok and apply you should be good. Also make sure that you are also running the code in release when you do this as well.

Credits/References:

Used Juce Framework to create UI. Credit to MatKatMusic for tutorials and pre-built for the EQ.
Link to EQ Repository: https://github.com/matkatmusic/SimpleEQ  

Referenced TheAudioProgrammer and his youtube video in order to start the Juce Plugin. (https://www.youtube.com/watch?v=pdSsPO9atYE&list=LL&index=2) 


UI of OneSend 3D Plugin:

Spectrum Analyzer: It is a real-time visual display of all frequencies (20Hz–20kHz) in the audio, showing their volume (dB) as peaks and valleys. This tool helps artists during both training and performance. For training, it reveals which frequencies and rhythms the AI is analyzing, and during use, it lets users visually track how their adjustments (like boosting bass or cutting highs) affect the overall sound of their audio (either imported or played on midi input).

Button with Blue Circle (Bypass Button): Used to mute certain parameters (low, high, peak) so that they do not have any influence on the audio processing. Can be clicked on and off.

Low Cut (Hz): Removes frequencies below the set value. The slider starts at the lowest frequency (20hz) and can be dragged up to the highest (20kHz).

Low Slope (db/oct): Determines how steeply the low-cut filter rolls off.

High Cut (Hz): Removes freq above set value. The slider starts at the highest frequency (20kHz) and can be dragged down to the lowest (20hz). 

High Slope (db/oct): Determines how steep the high cut filter rolls off.

Peak Freq (Hz): Picks which frequency to boost or cut.  Higher hz = Higher pitch sounds.

Peak Gain (db): Boosts the peak frequency if positive (+dB) or cuts it if negative (-dB).

Peak Quality: Controls how wide/narrow the frequency boost/cut is - high Q (narrow), low Q (wide).

Melodic/Rythmic Influence: Used for how much melodies and rythmic patterns influence the AI audio learning, not used in this frontend only part of the code.

Analyze: Used turn on/off the spectrum analyzer visually (audio will play).

Load/Stop Audio: Used to import an audio file (.wav, .mp3, .aiff, .flac) for audio processing and stop is used to clear the audio track of any audio playing.


