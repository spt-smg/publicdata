LAST UPDATED 2020/08/06 - JS

Since the full redshift distribution of the sample is now published, I have 
updated the source properties files to include all available spectroscopic
redshifts.

Some sources (SPT0128-51, SPT0404-59, SPT2052-56, SPT2146-56) were included in the original 

ALMA sample
but drop out of the "final" SPT sample due to a flux cut of S_870um > 25mJy; see
Reuter+2020. They remain in these files in order to match the published versions
and for completeness.

DESCRIPTION:

There are four files here containing the lens model parameters from Spilker+2016.

s16_lenses_individual.txt
This file has all of the parameters for each modeled lens, so sources with multiple
lenses are listed twice (labeled the same as in Table 3 of S+16). Not every source
has a lens redshift or source redshift, so those are marked with nan's. Redshifts 
are only needed to turn the Einstein radius into a lens mass. Lens positions are 
relative to the ALMA phase centers. Entries with zero uncertainty were held fixed 
during fitting.

s16_lenses_grouped.txt
This file combines all the lenses from each source. The only quantity that really
means anything in this case is the Einstein radius, so in this file they're just
summed in quadrature for each source. The uncertainties are propagated from the
MCMC chains directly. Entries with zero uncertainty were held fixed during fitting. 

s16_sources_individual.txt
This file has all the parameters for each 870um source, so there are multiple entries
if multiple sources were needed to model the ALMA data. If the source is lensed, its 
position is relative to the first lens in lenses_individual; if not, it's relative to 
the ALMA phase center. Entries with zero uncertainty were held fixed during fitting. 
Unlensed sources which were pointlike in the ALMA data also have zero size (you can 
take them as an upper limit on the size of <~0.2").

s16_sources_grouped.txt
In many cases, the multiple sources above are closer to approximating a complex source
structure rather than legitimately separate sources. This file "groups" related 
sources together (e.g., the two components of SPT0103-45), but keeps unrelated sources
separate (e.g., the two components of SPT0128-51). The distinction can be a bit
arbitrary, in principle, but I've tried to make it relatively straightforward. This file
gives the sum total flux per group, the quadrature sum of the source size, and the
flux-weighted 870um magnification. The uncertainties are propagated from the MCMC
chains directly, so they account for correlations between sources (and these values
are better than trying to compute these quantities yourself from the 
sources_individual file).