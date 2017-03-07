# DE1_SoC_Audio_Video

## Discription
This is the hardware project for de1soc audio test.

The linux driver code is locate at:https://github.com/hbwangjinwu/linux-socfpga/tree/alsa

The project original realease link is https://cloud.altera.com/devstore/platform/14.1.0/de1-soc-alsa-audio/ 

Thanks for Bsteinsbo developing the driver code.

## Compile

The hardware project should be compiled with the Quartus Prime. A sof file should be generated after compiling. And you can generate a .rbf file manually with executing the sof_to_rbf.bat file.

The linux code should be compiled with A linux PC or Virtual Machine.

The dtb file should also be generated in the linux kernel source by the command **make dtbs**.


## Setup
I tested it with the LXDE image. 

Copy the zImage and .dtb file to the SD card.

Copy the soc_system.rbf file to the SD card and Set the MSEL[4..0] to 00000.

First the mute function should be swithed off with the amixer or alsamixer .

The command should be like *amixer sset 'Output Mixer HiFi',0 on*

Then you can paly the wav with aplay tool or mdplay tool.

I have also tested playing .mp4 file.