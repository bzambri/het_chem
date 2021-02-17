# het_chem
## Some stuff for Doug's het chem project

Here's the Northern Hemisphere (NH) polar vortex for 2002-2003; the vortex edge is the thick black contour. Note that in most of November, the polar vortex is sort of barely there. And by April, too, it is all but gone. So I focused on JFM for the NH subpolar retrievals shown below. 

<p align="center"><img src="gifs/20021101.gif" alt="2002 NH polar vortex" width="75%"/></p>

Here's another example (2004-2005), which is similar if not a little bit more stable.

<p align="center"><img align="center" src="gifs/20041101.gif" alt="2004 NH polar vortex" width="75%"/></p>

<!---
The issue I was having is this: if you notice, there are periodically large PV values over the Himalayas. This is similar to what happens over the Andes in the SH, but the Andes run basically N-S, while the Himalayas have a much greater zonal extent. Anyway, all this meant was that I had to tweak the vortex edge definition a bit to make sure we weren't including profiles over the Himalayas in our distributions. Here are the results for that
--->

## HNO<sub>3</sub> profiles and PDFs
Here are Jan (excuse the aspect ratio), Feb, and March respectively:

<!---
![Jan_HNO3](images/MIPAS_HNO3_Vortex_01.eps)
--->
<img src="png/MIPAS_HNO3_Vortex_01.png" alt="Jan_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_02.png" alt="Feb_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_03.png" alt="Mar_HNO3_pdf"/>

And here are their CDFs (in all cases, all the CDFs are drawn from different distributions):

<p align="center"><img src="png/MIPAS_CDF_164-68_01.png" alt="Jan_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_02.png" alt="Feb_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_03.png" alt="Mar_HNO3_CDF" width="50%"/></p>

To Do:
- [ ] post monsoon plots
- [ ] check out SAGE3m NO<sub>2</sub> for the NH

