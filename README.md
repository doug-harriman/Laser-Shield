# Laser-Shield
Design documentation for a laser shield for the [Sainsmart Genmitsu 5.5W Laser Module](https://www.sainsmart.com/collections/cnc-machines/products/sainsmart-blue-laser-module-kit) mounted to a [Sainsmart Genmitsu 3018 Pro CNC Mill](https://www.sainsmart.com/collections/cnc-machines/products/sainsmart-genmitsu-cnc-router-pro-diy-kit).

![Laser Shield Rendering](https://github.com/doug-harriman/Laser-Shield/blob/main/images/Laser-Shield-small.png)


# BOM
|Part|Count|Material|
|:---| :-: |--------|
|Mount| 1 | PLA  |
|Front| 1 |Laser Shielding|
|Side| 2 |Laser Shielding|
|Rear| 1 |Laser Shielding|
|M3 Threaded Insert| 2 | Brass | 
|M3x8 Socket Head Screw| 2 | Stainless |

# Part Documentation
All parts were designed in Fusion360.  

## Mount 
The shield mount was 3D printed on a [Creality Ender3 Pro](https://www.creality3dofficial.com/products/creality-ender-3-pro-3d-printer) with [Hatchbox white PLA](https://www.amazon.com/gp/product/B00J0GMMP6/).

The STL was created in Fusion360 and sliced with [Cura](https://ultimaker.com/software/ultimaker-cura) 4.8.0 with the default settings for the Ender3 Pro and PLA, and a slice height of 0.12 mm.  Design files:
* [STL](mfg/Shield-Mount.stl)
* [G-Code](mfg/Shield-Mount.gcode) for 3D printer

## Front, Rear & Sides
The front, rear and side shields were machined out of a 300mm x 300mm sheet of laser shielding material on the Sainsmart Genmitsu 3018 Pro.

### Material
The laser shielding material is an transparent orange plastic which I believe to be cast acrylic. The laser wavelength is 445nm (blue).  Orange filters blue light eliminating most of the optical power.  Material was purchased from [J-Tech Photonics](https://jtechphotonics.com/?product=445nm-laser-shielding).

### Machining
* Tool
  * 1.0 mm diameter, 2 flute flat end mill.
  * Purchased on [Amazon](https://www.amazon.com/gp/product/B07KFVCHTT/).
* Feeds & Speeds
  * Spindle speed was at max using the stock 775 3018 Pro spindle motor.  This is approximately 5000 RPM.
  * Feed rates
    * Cutting: 600 mm/min
    * Positioning: 1500 mm/min
    * Depth of cut: 0.25 mm 
* Tool Path
  * Tool path used was a simple 2D contour, conventional (right) milling.  Details available in the Fusion360 design files.
  * G-Code 
    * [Front]() 
    * [Sides](mfg/shield-sides.nc) (machined together)
    * [Rear](mfg/shield-rear.nc)

## Threaded Inserts
M3 brass threaded inserts.  Purchased from [Amazon](https://www.amazon.com/gp/product/B07H2RWRW4/).

Inserts were pressed into the Mount with a soldering iron.  Pressed until they extended ~0.25 mm beyond the face of the Mount, then the Mount was pressed onto a flat surface to get the insert face flush and level with the Mount face.

## M3 Screws 
M3 hex socket head screws. Purchased from [Amazon](https://www.amazon.com/gp/product/B014OO5KQG).
