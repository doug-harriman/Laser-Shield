# Laser-Shield
Design documentation for a laser shield for a 3018 laser. 

![Laser Shield Rendering](https://github.com/doug-harriman/Laser-Shield/blob/main/images/Laser-Shield-small.png)


# BOM
|Part|Count|Material|Design File|
|:---| :-: |--------|-----------|
|Mount| 1 | PLA  ||
|Front| 2 |Laser Shielding||
|Side| 2 |Laser Shielding||
|Rear| 2 |Laser Shielding||
|M3 Threaded Insert| 2 | Brass | Purchased, see below|

# Part Documentation

## Front, Rear & Sides
The laser shielding material is an transparent orange plastic which I believe to be acrylic.  
The laser wavelength is 445nm (blue).  Orange filters blue light eliminating most of the optical power.

It was ordered from [J-Tech Photonics](https://jtechphotonics.com/?product=445nm-laser-shielding).

## Threaded Inserts
M3 brass threaded inserts.  Purchased from [Amazon](https://www.amazon.com/gp/product/B07H2RWRW4/).

## Mount 
The shield mount was printed on a [Creality Ender3 Pro](https://www.creality3dofficial.com/products/creality-ender-3-pro-3d-printer) with [Hatchbox white PLA](https://www.amazon.com/gp/product/B00J0GMMP6/).

The STL was created in Fusion360 and sliced with [Cura](https://ultimaker.com/software/ultimaker-cura) 4.8.0 with the default settings for the Ender3 Pro and PLA, and a slice height of 0.12 mm.  Design files:
* [STL](mfg/Shield-Mount.stl)
* [G-Code](mfg/Shield-Mount.gcode) for 3D printer
