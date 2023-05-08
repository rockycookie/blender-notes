# Vertices Overlap
I found this issue when trying to bisect an object into front part (with a hole), back part (with a hole) and middle connector (a cube that is supposed to be inserted into and thus connect the two other parts).

While Cura can load the exported STL files and I could see the holes on Cura. The hole on the front part exists after slicing but the hole on the back part disappeared after slicing. 

<br/>

## To fix the issue
It turns out (after a proof of concept prototyping) when I extrude the inner face to construct the hole on the back part, I somehow made duplicated vertices at the same or almost the same position.

Deleting the extra vertices on the same position and connect/fill the missing edges/faces fixed the issue. Silly small but time-consuming to debug (for me at that time) lol.
