# compressor
Audio compressor for Teensy
Based on https://github.com/MarkzP/AudioEffectDynamics

I fixed a bug where the compressor would pass no audio if the initial level was too low
It worked directly with audio from the Audio board, but not if the compressor was inserted after a filter 
A couple of the variables was NAN on init. 
The detection of a NAN variable is done with if (f != f) .... 
https://stackoverflow.com/questions/570669/checking-if-a-double-or-float-is-nan-in-c/570694

I also included some debug calls to print all the internal variables 
Also, I made some variables public and copied variables inside scopes out
