# het_chem
## het chem project update(s)

To do:
- [x] Compare MIPAS and WACCM profiles
- [x] 70-30 hPa
- [x] Plot individual years
- [ ] Apply changes to monsoon
- [ ] Spatial deNO<sub>y</sub>

1. [NH Subpolar](README.md#NH-subpolar)
   * [Profile discrepancy](README.md#profile-discrepancy)
   * [UTLS (164-68 hPa)](README.md#UTLS-(164-68-hPa))
      * [MIPAS HNO<sub>3</sub> PDFs](README.md#UTLS-MIPAS-HNO3-profiles-and-PDFs)
      * [MIPAS HNO<sub>3</sub> CDFs](README.md#UTLS-HNO3-CDFs)
   * [70-30 hPa](README.md#70-30-hPa)
      * [MIPAS HNO<sub>3</sub> PDFs](README.md#MIPAS-HNO3-profiles-and-PDFs)
      * [MIPAS HNO<sub>3</sub> CDFs](README.md#HNO3-CDFs)
   * [Individual years](README.md#individual-years)
1. [Monsoon HNO<sub>3</sub>](README.md#Monsoon)
<!---   * [SAGE3m NO<sub>2</sub>](README.md#SAGE3m-NO2) --->

## NH Subpolar

<!---
Here's the Northern Hemisphere (NH) polar vortex for 2002-2003; the vortex edge is the thick black contour. Note that in most of November, the polar vortex is sort of barely there. And by April, too, it is all but gone. So I focused on JFM for the NH subpolar retrievals shown below. 
<p align="center"><img src="gifs/20021101.gif" alt="2002 NH polar vortex" width="75%"/></p>
Here's another example (2004-2005), which is similar if not a little bit more stable.
<p align="center"><img align="center" src="gifs/20041101.gif" alt="2004 NH polar vortex" width="75%"/></p>
The issue I was having is this: if you notice, there are periodically large PV values over the Himalayas. This is similar to what happens over the Andes in the SH, but the Andes run basically N-S, while the Himalayas have a much greater zonal extent. Anyway, all this meant was that I had to tweak the vortex edge definition a bit to make sure we weren't including profiles over the Himalayas in our distributions. Here are the results for that
--->

### Profile discrepancy
There are substantially more profiles in WACCM compared to MIPAS. However, good days look, well, good:
<p align="center"><img src="png/MIPAS_NH_vortex_sample.png" alt="Jan_HNO3_pdf"/></p>
Red circles are WACCM, black circles are MIPAS. Pretty good match. But the problem is all the downtime that MIPAS had over its lifetime. The plot below shows the number of NH profiles for each day in WACCM (red), MIPAS (black), and the daily difference (blue):
<p align="center"><img src="png/nprof_MIPAS.png" alt="daily_nprofiles"/></p>
Essentially, there are many days where MIPAS is observing nothing but WACCM is observing the usual ~500 profiles in the NH. I changed my scripts to only report WACCM profiles on days when MIPAS also has at least 1 profile inside the vortex edge. As you'll see below, this helps but there are still more WACCM profiles than observed. So I may have to set a higher threshold (in the map above there are ~50 profiles...maybe 15 or more is a "good" day? I can look for a "bad" MIPAS day and plot that vs. WACCM), or I can match exact profile numbers.

### UTLS (164-68 hPa)
#### UTLS MIPAS HNO<sub>3</sub> profiles and PDFs
Here are Jan (excuse the aspect ratio), Feb, and March respectively:

<!---
![Jan_HNO3](images/MIPAS_HNO3_Vortex_01.eps)
--->
<img src="png/MIPAS_HNO3_Vortex_164-68_01.png" alt="Jan_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_02.png" alt="Feb_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_03.png" alt="Mar_HNO3_pdf"/>

#### UTLS HNO<sub>3</sub> CDFs 
In all cases, all the CDFs are drawn from different distributions:

<p align="center"><img src="png/MIPAS_CDF_164-68_01.png" alt="Jan_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_02.png" alt="Feb_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_164-68_03.png" alt="Mar_HNO3_CDF" width="50%"/></p>

### 70-30 hPa
#### MIPAS HNO<sub>3</sub> profiles and PDFs
Same as above, but the distribution plots are for 70-30 hPa. After looking at this, I could probably go to ~20 hPa. Anyway, these look really good! You were right Doug, looks like this is where the magic happens.

<!---
![Jan_HNO3](images/MIPAS_HNO3_Vortex_01.eps)
--->
<img src="png/MIPAS_HNO3_Vortex_70-30_01.png" alt="Jan_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_70-30_02.png" alt="Feb_HNO3_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_70-30_03.png" alt="Mar_HNO3_pdf"/>

#### HNO<sub>3</sub> CDFs 

<p align="center"><img src="png/MIPAS_CDF_70-30_01.png" alt="Jan_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_70-30_02.png" alt="Feb_HNO3_CDF" width="50%"/></p>
<p align="center"><img src="png/MIPAS_CDF_70-30_03.png" alt="Mar_HNO3_CDF" width="50%"/></p>

### Individual years
Below are the indiviual years for February. In general, WACCM varies a lot more than the obs.
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2003.png" alt="Jan_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2004.png" alt="Feb_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2005.png" alt="Mar_HNO3_pdf" width="50%"/>

<img src="png/MIPAS_HNO3_Vortex_164-68_01-2006.png" alt="Jan_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2007.png" alt="Feb_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2008.png" alt="Mar_HNO3_pdf" width="50%"/>

<img src="png/MIPAS_HNO3_Vortex_164-68_01-2009.png" alt="Jan_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2010.png" alt="Feb_HNO3_pdf" width="50%"/>
<img src="png/MIPAS_HNO3_Vortex_164-68_01-2011.png" alt="Mar_HNO3_pdf" width="50%"/>

<img src="png/MIPAS_HNO3_Vortex_164-68_01-2012.png" alt="Jan_HNO3_pdf" width="50%"/>

<!---
### SAGE3m NO<sub>2</sub>
As above, but for SAGE3m NO<sub>2</sub>
<img src="png/SAGE3m_NO2_Vortex01_164-72.png" alt="Jan_NO2_pdf"/>
<img src="png/SAGE3m_NO2_Vortex02_164-72.png" alt="Feb_NO2_pdf"/>
<img src="png/SAGE3m_NO2_Vortex03_164-72.png" alt="Mar_NO2_pdf"/>
If this is right (I think it is, but I will double-check everything), then it looks like everything in the NH is mixing of polar-subpolar air (see noHet60NS vs noHetAll below). I definitely would like to see what this looks like in the deNOy runs.
<img src="png/SAGE3m_CDF_02_164-72.png" alt="Feb_NO2_cdf"/>
--->

## Monsoon

Here are the PDF plots for June-September for 0-15N, Eastern Hemisphere only:

<img src="png/MIPAS_HNO3_Vortex_06_0-15N.png" alt="Jun_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_07_0-15N.png" alt="Jul_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_08_0-15N.png" alt="Aug_monsoon_pdf"/>
<img src="png/MIPAS_HNO3_Vortex_09_0-15N.png" alt="Sep_monsoon_pdf"/>



