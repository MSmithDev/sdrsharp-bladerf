sdrsharp-bladerf
================

bladeRF driver for SDR#


Installation
============

1. Copy the Release\SDRSharp.BladeRF.dll into SDR# installation directory
2. If required, copy all DLL files from LibBladeRF subdirectory to SDR# installation directory
3. Add the following line in the frontendPlugins sections of SDRSharp.exe.config file:

	&lt;add key="BladeRF" value="SDRSharp.BladeRF.BladeRFIO,SDRSharp.BladeRF" /&gt;


4. Launch SDR# and cross fingers :)

**Be aware that any update of SDR# will require you to follow again steps 2 to 4!**


Troubleshooting
===============

If your samples look "weird" under SDR#, be sure to use a compatible libusb-1.0.dll.
Specially when frequently upgrading SDR#, it will re-install the RTL-SDR driver which embedds a pretty old version of this DLL (v.1.0.14).
The version provided under LibBladeRF directory of this repository (currently v1.0.19) is known to work correcly with both RTL-SDR dongles and BladeRF. So it is safe (and recommended) to replace it.

If this does not solve your issue, feel free to report a bug here. I will try to fix it as soon as possible.
Same goes for new features.


Compilation
===========

If you need/want to compile this DLL, you need to copy the following two DLL files
from SDR# installation directory to Release and/or Debug directories:

1. SDRSharp.Radio.dll
2. SDRSharp.Common.dll
