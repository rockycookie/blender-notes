# Name Tag with Container

I am scaling everything by ensuring x-length is dboule of y-length.
And the final scaling is done in Cura, where I scaling uniformally by setting a certain x-length (so that we know y-length should be half of that).
Which helps me to print duplicate in a vertical column (every object share the same x-length).

After which, z-length can be then set in Cura not-uniformally if needed.

## Most recent setting
- case/container
    - x-length: 82mm
    - z-length: 22.96mm (set by uniformally x-length scale)
    - Scale ratio from Blender mesaurement:
        - Case inner x-length: ((200 - 2 * 6.23061) / 200) * 82 ~= 76.891mm
        - Case inenr y-length: 76.891mm / 2 ~= 38.445
        - Case inner z-length: (52 / 60) * 22.96 ~= 19.899mm 
- name tag (KevinP & KevinZ)
    - x-length: 75mm
    - y-length: 75mm / 2 = 37.5
    - z-length: 18mm

## Printing profile
- line hight: 0.1mm
- line width: 0.4mm
- wall thicness: 0.5mm

## Comment & Note
- I was lucky that this name tag can fit into the case with basically no extra space
- Note the software decided x,z dimensions of the name tag is a bit more than 1.5mm (but less than 2mm) smaller than the x,z dimentions of the container
    - y dimentsion of the name tag is a bit less than 1mm smaller than the case
- The inner x-length calculation is kind of wrong because the coners of the container was beveled and thus I need to calculate the shortest distancebetween the 2 corners instead of the longest distance as I did in the sample above
