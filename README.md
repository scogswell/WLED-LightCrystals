# WLED-LightCrystals
Platformio configuration for compiling MoonModules WLED for UM Light Crystals Kit  https://unexpectedmaker.com/shop.html#!/Light-Crystals-Kit/p/701883350

Use with the MoonModules version of WLED https://github.com/MoonModules/WLED

Drop this file into the WLED directory, and the MoonModules WLED project should pick it up and use it. No other source modifications are necessary. 

You can compile for the Light Crystals after installing all the WLED prequisites in PlatformIO by changing the target to `esp32s3_UM_LIGHTCRYSTALS_8MB_PSRAM_qspi`

This override contains all the proper pin numbers to configure the Light Crystals out-of-the-box to work with WLED including the LEDs and the microphone.  

After compiling and flashing the Light Crystals board there are some post setup things you still have to do:

* Set your wifi network 
* Set the 2D layout to 9x9 (I mean, if you want to, you don't have to unless you want to use the Light Crystals as a 2D matrix)
* Enable the I2S microphone in Audioreactive settings. 
* have fun with your Light Crystals

If you choose to, you can use the "Config" -> "Security and Updates" section of the WLED web interface and upload these files which will do some more setup:
* Presets (really just one preset as a demo): `wled_presets_WLED-LIGHTCRYSTALS.json`
* Configuration (will set the 2D layout and enable the mic): `wled_cfg_WLED-LIGHTCRYSTALS.json`

The configuration `.json` files here don't set any WiFi network, so you should still do that. 