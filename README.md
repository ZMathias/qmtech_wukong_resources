# Constraint file (xdc)
The repository contains a basically complete xdc file for the development board pieced together from the official design schematics and example projects found in the [official repository](https://github.com/ChinaQMTECH/QM_XC7A100T_WUKONG_BOARD). The constraint file was generated using Gemini, so please double check this first if something isn't working as expected.

The repository also contains a udev rule file for linux users that are programming this using the standard Xilinx platform cable JTAG programmer. This is needed to give Vivado permissions to use this device through USB.
Copy the file to `/etc/udev/rules.d/` then run the following commands:
```
sudo udevadm control --reload-rules
sudo udevadm trigger
```

Unplug the programmer, then back in and it should work. Vivado might throw an error regarding incorrect hw_server version. Ignore it and try to connect again. Flashing is slow, be patient.
