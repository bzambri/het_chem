# het_chem
## Some stuff for Doug's het chem project

1. [NH Subpolar](README.md#NH-subpolar)
   * [MIPAS HNO<sub>3</sub> PDFs](README.md#MIPAS-HNO3-profiles-and-PDFs)
   * [MIPAS HNO<sub>3</sub> CDFs](README.md#HNO3-CDFs)
   * [SAGE3m NO<sub>2</sub>](README.md#SAGE3m-NO2)
1. [Monsoon HNO<sub>3</sub>](README.md#Monsoon)

## NH Subpolar

Here's the Northern Hemisphere (NH) polar vortex for 2002-2003; the vortex edge is the thick black contour. Note that in most of November, the polar vortex is sort of barely there. And by April, too, it is all but gone. So I focused on JFM for the NH subpolar retrievals shown below. 

<p align="center"><img src="gifs/20021101.gif" alt="2002 NH polar vortex" width="75%"/></p>

Here's another example (2004-2005), which is similar if not a little bit more stable.

<p align="center"><img align="center" src="gifs/20041101.gif" alt="2004 NH polar vortex" width="75%"/></p>

<!---
The issue I was having is this: if you notice, there are periodically large PV values over the Himalayas. This is similar to what happens over the Andes in the SH, but the Andes run basically N-S, while the Himalayas have a much greater zonal extent. Anyway, all this meant was that I had to tweak the vortex edge definition a bit to make sure we weren't including profiles over the Himalayas in our distributions. Here are the results for that
--->

### MIPAS HNO<sub>3</sub> profiles and PDFs
Here are Jan (excuse the aspect ratio), Feb, and March respectively:

<!---
![Jan_HNO3](images/MIPAS_HNO3_Vortex_01.eps)
--->
<img src="png/MIPAS_HNO3_Vortex_01.png" alt="Jan_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_02.png" alt="Feb_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_03.png" alt="Mar_HNO3_pdf"/>

Besides the clear indication of heterogeneous processing (compare to noHetChem), I think the most noticeable thing here is the bump in HNO3 in Feb and especially March in WACCMhet008.

### HNO<sub>3</sub> CDFs 
In all cases, all the CDFs are drawn from different distributions:

<p align="center"><img src="png/MIPAS_CDF_164-68_01.png" alt="Jan_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_02.png" alt="Feb_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_03.png" alt="Mar_HNO3_CDF" width="50%"/></p>

### SAGE3m NO<sub>2</sub>
As above, but for SAGE3m NO<sub>2</sub>
<img src="png/SAGE3m_NO2_Vortex01_164-72.png" alt="Jan_NO2_pdf"/>
<img src="png/SAGE3m_NO2_Vortex02_164-72.png" alt="Feb_NO2_pdf"/>
<img src="png/SAGE3m_NO2_Vortex03_164-72.png" alt="Mar_NO2_pdf"/>
If this is right (I think it is, but I will double-check everything), then it looks like everything in the NH is mixing of polar-subpolar air (see noHet60NS vs noHetAll below). I definitely would like to see what this looks like in the deNOy runs.
<img src="png/SAGE3m_CDF_02_164-72.png" alt="Feb_NO2_cdf"/>


## Monsoon

Here are the PDF plots for June-September for 0-15N, Eastern Hemisphere only:

<img src="png/MIPAS_HNO3_Vortex_06_0-15N.png" alt="Jun_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_07_0-15N.png" alt="Jul_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_08_0-15N.png" alt="Aug_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_09_0-15N.png" alt="Sep_monsoon_pdf"/>

To Do:
- [x] post monsoon plots
- [x] check out SAGE3m NO<sub>2</sub> for the NH
- [ ] check num profiles for 008 run (sunrise/sunset?)

