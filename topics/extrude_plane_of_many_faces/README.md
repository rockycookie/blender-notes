# Extrude a plane with many faces
I found it difficult to select multiple faces at the same plane and extrdue them normally, which usually leads to faces extrdued to different directions and they are weirdly connected.

Note, later I learned `Solidify` lol~

## Initial walk-around
In stead of extruding faces, extrude vertices, like:
![example](./extrude-vertices-instead-of-faces.PNG)
This is teribly slow, DONT DO!

## Using solidify
<s>Using `solidify` modifier could give a thickness to a plane but Cura currently does not recognize the thickness.</s>

Note, `solidify` is the correct and more-convenient alternative to face extruding; it did not work for me initially because I simply did not click on `apply` (the button was hidden in a dropdown lol).
But `solidify` will get the same issue due to the same reason.

## Eventual solution
It turns out the faces are extruded to different directions because

1. There are overlapping vertices and edges --> We can simply merge those vertices by `Ctrl` + `m` and select merging by distance (with a good distance to merge, note the default value could be too small).
2. If a line cross a face but does not divide the face --> Fix is simply to make the line divide the face into 2; currently I am deleting the face and fill the 2 divided faces again

Extruding multiple faces (Solidify) then should be working as expected (to the same direction).

Cheers!
