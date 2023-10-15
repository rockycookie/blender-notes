# Extrude a plane with many faces
I found it difficult to select multiple faces at the same plane and extrdue them normally, which usually leads to faces extrdued to different directions and they are weirdly connected.

## Initial walk-around
In stead of extruding faces, extrude vertices, like:
![example](./extrude-vertices-instead-of-faces.PNG)

## Short cut which does not work with Cura
Using `solidify` modifier could give a thickness to a plane but Cura currently does not recognize the thickness.

## Eventual solution
It turns out the faces are extruded to different direction because there are overlapping vertices and edges, we can simply merge those vertices by `Ctrl` + `m` and select merging by distance (with a good distance to merge, note the default value could be too small).
Extruding multiple faces then should be working as expected (to the same direction).

Cheers!
