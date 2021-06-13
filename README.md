# Laser-Shield
Design documentation for a laser shield for the [Sainsmart Genmitsu 5.5W Laser Module](https://www.sainsmart.com/collections/cnc-machines/products/sainsmart-blue-laser-module-kit) mounted to a [Sainsmart Genmitsu 3018 Pro CNC Mill](https://www.sainsmart.com/collections/cnc-machines/products/sainsmart-genmitsu-cnc-router-pro-diy-kit).  See my [3018 Mill](https://github.com/doug-harriman/3018-Mill/) repository for general information about using the mill and laser.

![Laser Shield Rendering](https://github.com/doug-harriman/Laser-Shield/blob/main/images/Laser-Shield-small.png)
![Laser Shield Photo](https://github.com/doug-harriman/Laser-Shield/blob/main/images/photo-iso-small.jpg)

![Laser Shield In Use](https://github.com/doug-harriman/Laser-Shield/blob/main/images/in-use-small.jpg)

# BOM
|Part|Count|Material|
|:---| :-: |--------|
|Mount| 1 | PLA  |
|Front| 1 |Laser Shielding|
|Side| 2 |Laser Shielding|
|Rear| 1 |Laser Shielding|
|M3 Threaded Insert| 2 | Brass | 
|M3x6 Screw| 2 | Stainless |

# Part Documentation
All parts were designed in Fusion360, see the [cad](cad/) directory for CAD files.

Assembly [STL](cad/laser-shield-v25.stl)

## Mount 
The shield mount was 3D printed on a [Creality Ender3 Pro](https://www.creality3dofficial.com/products/creality-ender-3-pro-3d-printer) with [Hatchbox white PLA](https://www.amazon.com/gp/product/B00J0GMMP6/).

The STL was created in Fusion360 and sliced with [Cura](https://ultimaker.com/software/ultimaker-cura) 4.8.0 with the default settings for the Ender3 Pro and PLA, and a slice height of 0.12 mm.  Design files:
* [STL](cad/Shield-Mount.stl)
* [G-Code](mfg/Shield-Mount.gcode) for 3D printer

## Front, Rear & Sides
The front, rear and side shields were machined out of a 300mm x 300mm sheet of laser shielding material on the Sainsmart Genmitsu 3018 Pro.

STL for:
* [Front](cad/Shield-Front.stl)
* [Sides](cad/Shield-Side.stl)
* [Rear](cad/Shield-Rear.stl)

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
    * [Front](/mfg/shield-front.nc) 
    * [Sides](mfg/shield-sides.nc) (machined together)
    * [Rear](mfg/shield-rear.nc)

## Threaded Inserts
M3 brass threaded inserts.  Purchased from [Amazon](https://www.amazon.com/gp/product/B07H2RWRW4/).

Inserts were pressed into the Mount with a soldering iron.  Pressed until they extended ~0.25 mm beyond the face of the Mount, then the Mount was pressed onto a flat surface to get the insert face flush and level with the Mount face.

## M3 Screws 
M3x6 hex socket head screws. Purchased from [Amazon](https://www.amazon.com/gp/product/B014OO5KQG).

# Artwork
All artwork was created in Inkscape and converted from SVG to G-Code with the Lasertools Inkscape Extension.  See my [3018 Mill](https://github.com/doug-harriman/3018-Mill/) project for more information on the tools and processes.

Portions of the artwork were obtained from the Open Source community.  See the [Artwork Source](artwork/artwork-source.md) documentation for more details.

Laser etch parameters (see 3018 Mill project for speed & power test data)
* Etching speed: 800 mm/min (infill & perimeter)
* Infill laser power: 40% (400 on Sainsmart system)
* Perimeter laser power: 60% (600 on Sainsmart system)
* Beam width: 0.2 mm
* Contour tolerance: 0.1 mm

# Future Improvements
* Redesign rear shield to mount fan for air assist for cutting.
  * Have a small fan on hand from [Amazon](https://www.amazon.com/gp/product/B0755BY9RH/). 
* Reduce length of shield mount.  Interferes with top of Z-axis mount when in extreme +Z position.

# Links
Other links to this project
* [YouTube](https://www.youtube.com/watch?v=rP4ZKo0Rn4E)
* [Thingiverse](https://www.thingiverse.com/thing:4885034)
