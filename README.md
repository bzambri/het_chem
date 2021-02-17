# het_chem
## Some stuff for Doug's het chem project

Here's the Northern Hemisphere (NH) polar vortex for 2002-2003; the vortex edge is the thick black contour. Note that in most of November, the polar vortex is sort of barely there. And by April, too, it is all but gone. So I think we need to focus on (D)JFM for these subpolar retrievals in the NH. 

![2002 NH polar vortex](gifs/20021101.gif)

Here's another example (2004-2005), which is similar if not a little bit more stable.

![2004 NH polar vortex](gifs/20041101.gif)

The issue I was having is this: if you notice, there are periodically large PV values over the Himalayas. This is similar to what happens over the Andes in the SH, but the Andes run basically N-S, while the Himalayas have a much greater zonal extent. Anyway, all this meant was that I had to tweak the vortex edge definition a bit to make sure we weren't including profiles over the Himalayas in our distributions. Here are the results for that

## HNO_3 profiles and PDFs
