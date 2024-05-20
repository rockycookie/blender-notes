# Extrude a plane with many faces
I found it difficult to select multiple faces at the same plane and extrdue them normally, which usually leads to faces extrdued to different directions and they are weirdly connected.

## Initial walk-around
In stead of extruding faces, extrude vertices, like:
![example](./extrude-vertices-instead-of-faces.PNG)

## Using solidify
<s>Using `solidify` modifier could give a thickness to a plane but Cura currently does not recognize the thickness.</s>

Note, `solidify` is the correct and more-convenient alternative to face extruding; it did not work for me initially because I simply did not click on `apply` (the button was hidden in a dropdown lol).
But `solidify` will get the same issue due to the same reason.

## Eventual solution
It turns out the faces are extruded to different direction because there are overlapping vertices and edges, we can simply merge those vertices by `m` and select merging by distance (with a good distance to merge, note the default value could be too small).
Extruding multiple faces then should be working as expected (to the same direction).

Cheers!
