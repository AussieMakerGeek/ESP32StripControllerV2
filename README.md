# ESP32StripControllerV2
Visual Pinball Stripcontroller on ESP32 WROOM-32

A Fork of https://github.com/elbirk/ESP32StripController with some improvements which was originally a ported version of TeensyStripController for ESP32 WROOM-32

Original version found on.
https://github.com/DirectOutput/TeensyStripController

As at upload, this code is completely untested - Do not use it. It will be updated once I can establish a test platform.

Should be fixed:

1. DOF cannot change Striplength, you have to alter the code. This is because I to late discovered that FASTLED library cannot change the strip length dynamically. So either I need to find a new libary or make a hack for fastled - *Implemented by using FastLed.setLeds() function*
2. Version that do not use special directoutput.dll - *The code changes I have made reflect the same functions as the original (other than the 'T' function implemented by elbirk), I don't see how this is still needed. Waiting confirmation from elbirk. My only thought was that perhaps it's related to the com port speed but this is actually configurable in DOF xml config (Not documented, but shows in source code).*
