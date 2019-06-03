follow the instruction here to build:

http://wiki.friendlyarm.com/wiki/index.php/Building_U-boot_and_Linux_for_H5/H3/H2%2B

just replace friendlyarm/linux to zexee/linux

Note that both sound card driver and dts are changed.
dts only changed for nanopi-neo-air

force in i2s slave mode, bclk and lclk as input
force in i2s input mode, offset 1 bit

test using

sudo arecord -D hw:4 -r 48000 -f S32_LE -c 2 a.wav
