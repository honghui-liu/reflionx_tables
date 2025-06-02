# Grid tables for the local disk reflection model `reflionx`

Five tables are provided for the `reflionx` model. They can be downloaded from: https://github.com/honghui-liu/reflionx_tables/releases/tag/table

## Main models

1. `reflionx_HD_nthcomp_v2_log.fits`
    - The input spectrum is a `nthcomp`with the **photon index**, the blackbody **seed photon temperature** (kT_bb) and coronal temperature (kT_e) as free parameters.
    - The **electron density and the iron abundance are free parameters**.
    - Please cite:
        - Ross & Fabian, 2007, MNRAS, 381, 1697 [link](https://ui.adsabs.harvard.edu/abs/2007MNRAS.381.1697R/abstract)
        - (First application in) Jiang, 2020, MNRAS, 498, 3888 [link](https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.3888J/abstract)

2. `reflionx_bb.mod`
    - The input spectrum is a single-temperature blackbody. 
    - Free parameters are the blackbody temperature (kT), the iron abundance and the ionization parameter.
    - Usually, the model is used to fit the reflection component in neutron star systems (e.g., in combination with the relativistic broadening kernel `relconv*atable{reflionx_bb}`). Occasionally, it is also applied to model the reflection component in the soft state of black hole systems to account for the effect of returning radiation—although this is, of course, a simplification.
    - Please cite
        - Ross & Fabian, 2005, MNRAS, 358, 211. [link](https://ui.adsabs.harvard.edu/abs/2005MNRAS.358..211R/abstract)
        - (First application in) King, et al., 2016, ApJ, 819, 29. [link](https://ui.adsabs.harvard.edu/abs/2016ApJ...819L..29K/abstract)
    - **Note:** There is similar version of model calculated by Prof. Ballantyne (BBrefl, [link](https://heasarc.gsfc.nasa.gov/docs/xanadu/xspec/models/bbrefl.html)), which is also based on the `reflionx` code. The differences between `reflionx_bb` and `BBrefl` are explained in Garcia et al. 2022, ApJ, 926, 13 (see Section 3.3.1 on page 7 in [link](https://ui.adsabs.harvard.edu/abs/2022ApJ...926...13G/abstract)). The main differences are:
        - `BBrefl` assumes local thermodynamical equilibrium (LTE) throughout the slab while `reflionx_bb` does not.
        - `reflionx_bb` has a broader range of parameters (e.g., density and ionization) and considers more elements and charge states.

## Previous models

3. `reflionx.mod`
    - The input spectrum is a `cutoffpl` with the cutoff energy fixed at 300 keV.
    - The electron density is fixed at 10^15 cm^-3.
    - Free parameters are the photon index, the iron abundance (in solar units) and the ionization parameter.
    - This model is identical to the one hosted on the Heasarc "Additional Models" website.
    - Please cite:
        - Ross, Fabian and Young, 1999, MNRAS, 306, 461. [link](https://ui.adsabs.harvard.edu/abs/1999MNRAS.306..461R/abstract)
        - Ross & Fabian, 2005, MNRAS, 358, 211. [link](https://ui.adsabs.harvard.edu/abs/2005MNRAS.358..211R/abstract)   

4. `reflionx_HD.mod`
    - The input spectrum is a `cutoffpl` with the cutoff energy fixed at 300 keV.
    - The **electron density is a free parameter**, while the iron abundance is fixed at solar value.
    - Free parameters are the photon index, the electron density and the ionization parameter.
    - Please cite:
        - Ross & Fabian, 2007, MNRAS, 381, 1697 [link](https://ui.adsabs.harvard.edu/abs/2007MNRAS.381.1697R/abstract)
        - (First application in) Tomsick, 2018, ApJ, 855, 3. [link](https://ui.adsabs.harvard.edu/abs/2018ApJ...855....3T/abstract)

5. `reflionx_hc.mod`
    - The input spectrum is a `cutoffpl` with a **variable cutoff energy**.
    - The electron density is fixed at 10^15 cm^-3.
    - Free parameters are the photon index, the cutoff energy, the iron abundance and the ionization parameter. **Note that the iron abundance can go up to 30 times of the solar value.**
    - Please cite:
        - Ross & Fabian, 2005, MNRAS, 358, 211. [link](https://ui.adsabs.harvard.edu/abs/2005MNRAS.358..211R/abstract)
        - (First application in) Tomsick, et al., 2014, 780, 78. [link](https://ui.adsabs.harvard.edu/abs/2014ApJ...780...78T/abstract)



The tables can be loaded into `XSPEC` with the `atable` function.

## Examples of using the grids:

### XRBs

**Black hole systems:**

- Cygnus X-1
    - Tomsick et al. 2018, ApJ, 855, 3. [link](https://ui.adsabs.harvard.edu/abs/2018ApJ...855....3T/abstract)
- GX 339-4
    - Jiang et al. 2019, MNRAS, 484, 1972. [link](https://ui.adsabs.harvard.edu/abs/2019MNRAS.484.1972J/abstract)
    - Liu et al. 2022, MNRAS, 513, 4308. [link](https://ui.adsabs.harvard.edu/abs/2022MNRAS.513.4308L/abstract)
- GRS 1716-249
    - Jiang et al. 2020, MNRAS, 492, 1947. [link](https://ui.adsabs.harvard.edu/abs/2020MNRAS.492.1947J/abstract)
- EXO 1846-031
    - Draghis et al. 2020, ApJ, 900, 78. [link](https://ui.adsabs.harvard.edu/abs/2020ApJ...900...78D/abstract)
- 4U 1630-47
    - Connors et al. 2021, ApJ, 909, 146. [link](https://ui.adsabs.harvard.edu/abs/2021ApJ...909..146C/abstract)
- MAXI J1348-630
    - Chakraborty et al. 2021, MNRAS, 508, 475. [link](https://ui.adsabs.harvard.edu/abs/2021MNRAS.508..475C/abstract)
- MAXI J1813-095
    - Jiang et al. 2022, MNRAS, 514, 1952. [link](https://ui.adsabs.harvard.edu/abs/2022MNRAS.514.1952J/abstract)
- MAXI J1535–571, GRS 1739–278, GS 1354–64, IGR J17091–3624, H 1743–322, V404 Cyg
    - Liu et al. 2023, ApJ, 951, 145. [link](https://ui.adsabs.harvard.edu/abs/2023ApJ...951..145L/abstract)
 
**Neutron star systems:**
- 4U 1728-34
    - Wang et al. 2019, MNRAS, 484, 3004. [link](https://ui.adsabs.harvard.edu/abs/2019MNRAS.484.3004W/abstract)
- Cygnus X-2
    - Mondal et al. 2018, MNRAS, 474, 2064. [link](https://ui.adsabs.harvard.edu/abs/2018MNRAS.474.2064M/abstract)
    - Ludlam et al. 2022, ApJ, 927, 112. [link](https://ui.adsabs.harvard.edu/abs/2022ApJ...927..112L/abstract) 

### AGNs

- IRAS 13224−3809
    - Jiang et al. 2022, MNRAS, 514, 1107. [link](https://ui.adsabs.harvard.edu/abs/2022MNRAS.514.1107J/abstract)
- Ultra-Soft Narrow-Line Seyfert 1s
    - Jiang et al. 2020, MNRAS, 498, 3888. [link](https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.3888J/abstract) 
  
