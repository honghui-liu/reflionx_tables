# Grid tables for the local disk reflection model `reflionx`

Five tables are provided for the `reflionx` model. They can be downloaded from: https://github.com/honghui-liu/reflionx_tables/releases/tag/table

1. `reflionx.mod`
    - The input spectrum is a `cutoffpl` with the cutoff energy fixed at 300 keV.
    - The electron density is fixed at 10^15 cm^-3.
    - Free parameters are the photon index, the iron abundance and the ionization parameter.
    - This model is identical to the one hosted on the Heasarc "Additional Models" website.
    - Please cite: Ross & Fabian, 2005, MNRAS, 358, 211. [link](https://ui.adsabs.harvard.edu/abs/2005MNRAS.358..211R/abstract)

2. `reflionx_HD.mod`
    - The input spectrum is a `cutoffpl` with the cutoff energy fixed at 300 keV.
    - The **electron density is a free parameter**, while the iron abundance is fixed at solar value.
    - Free parameters are the photon index, the electron density and the ionization parameter.
    - Please cite: Tomsick, 2018, ApJ, 855, 12. [link](https://ui.adsabs.harvard.edu/abs/2018ApJ...855....3T/abstract)

3. `reflionx_hc.mod`
    - The input spectrum is a `cutoffpl` with a **variable cutoff energy**.
    - The electron density is fixed at 10^15 cm^-3.
    - Free parameters are the photon index, the cutoff energy, the iron abundance and the ionization parameter.
    - Please cite: (one of Michael's papers)

4. `reflionx_HD_nthcomp_v2_log.fits`
    - The input spectrum is a `nthcomp`with the **photon index**, the blackbody **seed photon temperature** (kT_bb) and coronal temperature (kT_e) as free parameters.
    - The **electron density and the iron abundance are free parameters**.
    - Please cite: Jiang, 2020, MNRAS, 498, 3888 [link](https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.3888J/abstract)

5. `reflionx_bb.mod`
    - The input spectrum is a single-temperature blackbody. 
    - Free parameters are the blackbody temperature (kT), the iron abundance and the ionization parameter.
    - Please cite: Ross & Fabian, 2005, MNRAS, 358, 211. [link](https://ui.adsabs.harvard.edu/abs/2005MNRAS.358..211R/abstract)



The tables can be loaded into `XSPEC` with the `atable` function.

To use any of the models above, please cite:
- Ross, Fabian and Young, 1999, MNRAS, 306, 461. [link](https://ui.adsabs.harvard.edu/abs/1999MNRAS.306..461R/abstract)

Examples of using the grids:
- Jiang et al. 2019, MNRAS, 484, 1972. [link](https://ui.adsabs.harvard.edu/abs/2019MNRAS.484.1972J/abstract)
- Jiang et al. 2019, MNRAS, 489, 3436. [link](https://ui.adsabs.harvard.edu/abs/2019MNRAS.489.3436J/abstract)
- Liu et al. 2023, ApJ, 951, 145. [link](https://ui.adsabs.harvard.edu/abs/2023ApJ...951..145L/abstract)
