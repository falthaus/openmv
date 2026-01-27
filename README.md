# openmv

Fork of the [openmv firmware repository](https://github.com/openmv/openmv).


## Modifications

- [omv_csi.c](common/omv_csi.c): for the OpenMV Cam H7 (`TARGET=OPENMV4`) the framebuffer
is allocated as 1 byte/pixel (instead of the default 2 bytes/pixel) to enable fitting a full
resolution grayscale image into the limited memory (tested with VG and WVGA2).


<p>&nbsp;</p>


## Constraints

- Only `GRAYSCALE` pixel format is supported on the OpenMV Cam H7. Everything else
will result in a RuntimeError: "Frame buffer overflow, try reducing the frame size",
no matter the actual frame size setting.


<p>&nbsp;</p>
