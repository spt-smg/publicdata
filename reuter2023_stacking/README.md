Reuter et al. (2023)
====================================

[ADS](https://ui.adsabs.harvard.edu/abs/2023ApJ...948...44R/abstract) | [arXiv](https://arxiv.org/abs/2210.11671)

In this paper, we present the full stacked sub/mm spectrum of 78 of the SPT DSFG catalog (all DSFGs with 3mm ALMA spectra).  This paper is essentially an update from the original stacked spectrum presented in [Spilker et al. 2014](https://ui.adsabs.harvard.edu/abs/2014ApJ...785..149S/abstract) of 22 high-redshift dusty galaxies based on Cycle 0 ALMA 3mm data.  In subsequent years, we have been able to get 3mm spectra (and redshifts) for the complete sample of SPT DSFGs, which were presented in [Reuter et al. 2020](https://ui.adsabs.harvard.edu/abs/2020arXiv200614060R/abstract).  In this update, we revisited Justin's faint line analysis, and CO SLEDs.  

This repo contains the stacked spectrum (Fig. 4), the faint lines (Table B1) and the updated CO SLED (from Fig. 5) from Reuter et al. 2023.  


Questions about this data can be directed to Cassie: [creuter@illinois.edu](mailto:creuter@illinois.edu)

Updates
--------

Since the redshift for SPT0452-50 was found in [Riechers+24](https://ui.adsabs.harvard.edu/abs/2024arXiv240105487R/abstract) to be z=5.0160, we have adjusted the stacked spectrum .txt file and figure with the corresponding 3mm spectrum at the correct frequency.  We also adjusted the molecular line detections in both the CO SLED and faint line (Table B1) tables.  Because SPT0452-50 originally was an outlier with $\mathrm{T_{dust}} = 21$ K and $\mathrm{M_{dust}} = 3 \times 10^{10} \, \mathrm{M_\odot}$ and the stacked spectrum was weighted by dust mass, this source contributed significantly to the flux density of the stacked 12CO(3-2) and 12CO(1-0) lines.  The updated version of the 12CO SLED reflects both updated redshift (changing the transitions of CO lines we observed) and dust mass ($\mathrm{M_{dust}}$ = $1.8 \times 10^9$ $\mathrm{M_\odot}$, see the [Reuter+2020 repository](https://github.com/spt-smg/publicdata/tree/updated0452/reuter2020_final_dndz) for details).  For simplicity, we omit SPT0452-50 from the faint line detections.  The updated values agree with the published values within the stated errors.  

Citation
--------

```
@ARTICLE{2023ApJ...948...44R,
       author = {{Reuter}, C. and {Spilker}, J.~S. and {Vieira}, J.~D. and {Marrone}, D.~P. and {Weiss}, A. and {Aravena}, M. and {Archipley}, M.~A. and {Chapman}, S.~C. and {Gonzalez}, A. and {Greve}, T.~R. and {Hayward}, C.~C. and {Hill}, R. and {Jarugula}, S. and {Kim}, S. and {Malkan}, M. and {Phadke}, K.~A. and {Stark}, A.~A. and {Sulzenauer}, N. and {Vizgan}, D.},
        title = "{The Rest-frame Submillimeter Spectrum of High-redshift, Dusty, Star-forming Galaxies from the SPT-SZ Survey}",
      journal = {\apj},
     keywords = {Interstellar medium, Strong gravitational lensing, Ultraluminous infrared galaxies, Cosmology, Astrochemistry, 847, 1643, 1735, 343, 75, Astrophysics - Astrophysics of Galaxies},
         year = 2023,
        month = may,
       volume = {948},
       number = {1},
          eid = {44},
        pages = {44},
          doi = {10.3847/1538-4357/acaf51},
archivePrefix = {arXiv},
       eprint = {2210.11671},
 primaryClass = {astro-ph.GA},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2023ApJ...948...44R},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}



```
