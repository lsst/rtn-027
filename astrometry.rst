.. _section-sfm-astrom-vv:
Single Frame Processing: Astrometry V&V
=======================================

A detailed investigation on the quality of the astrometric calibration of the Single Frame Processing (SFP) stage of the Rubin Observatory :abbr:`LSST (Legacy Survey of Space and Time)` Science Pipelines was performed on the `PREOPS-850 <https://jira.lsstcorp.org/browse/PREOPS-850/>`__ Jira ticket.  The analysis is based on the processing of test datasets with the aim of asserting the fidelity of the Science Pipelines before kicking off the SFP of the full DP0.2 dataset.  A brief summary of the findings is provided here.  Please refer to that ticket for further plots and details.  Note that this investigation does not include any measurement or assessment of the "Key Performance Metrics" defined in DOCUMENT?, which largely involve the inter-visit repeatablility statistics.  These will be computed using the `faro <https://github.com/lsst/faro>`__ package and reported ELSEWHERE.

The executive summary is that, as of the ``v23_0_0_rc3`` tag of the LSST Science Pipelines, the DP0.2 V&V team asserts that the quality of the astrometric calibration per detector/visit for SFP meets expectations for the SFP of the full DP0.2 dataset to proceed.

The following subsections describe a few of the "metrics" used to qualify the above statement.

Mean On-Sky Distance: Reference vs. Source
------------------------------------------

An examination of the distrubutions of the mean on-sky distance (in arcsec) between matched source and reference objects post-fit, for the entire test sample as well as per-band.

Of note was the identification of two detectors as astrometric "outliers", in that they had mean on-sky distances well outside the range covered by the rest of the sample.  We very much want to avoid having detectors with bad calibrations polluting the coadds, so an action was taken to add a threshold on this metric above which the astrometric fit is deemed a "failure", keeping calibrated visit-level exposures from consideration in coaddition.  Following the implementation, the two outliers did indeed disappear from the outputs with no other changes observed (as desired).  The resulting distribution of the mean on-sky distance has a maximum value of ``~0.02 arcsec`` (which may seem almost too good to anyone familiar with even the highest-quality real datat, but because of the nature of the simulations and the "perfectness" of the reference catalog, this value does make sense in this context).

The following plots show the before (two outliers observed) and after (two outliers now gone):

.. figure:: /_static/astrometryPlots/astromDistMeanVsStd_4431_rc2_vs_rc3.png
   :width: 800
   :name: fig-astrom-distance-std-vs-mean

Standard deviation versus mean on-sky distance between reference and matched sources for SFP astrometric calibration. Left: pre-thresholding.  Right: post-thresholding.


WCS scatter as a funtion of position on the focal plane
-------------------------------------------------------

The following plots the mean astrometry distance as a function of position in the focal plane:

.. figure:: /_static/astrometryPlots/astromDistanceMeanFP_4431.png
   :width: 300
   :name: fig-astrom-distance-fp
   :target: ../_images/astromDistanceStdVsMeanAllBands_4431.png

Distribution of the mean astrometry distance as a function of position in the focal plane.  Each visit/detector gets a single point and, for visualization purposes, the position each point is staggered within the detector boundaries.

No trend with position on the focal plane is observed.

The investigation on the ticket went a bit deeper into issues related to the camera geometry currently implemented for ``LSSTCam-imSim`` by looking at the difference between the raw and SFP-calibrated WCSs.  It is known that the simulations include a radial distortion and this does turn up in analysi (vizualized with quiver plots of vectors from raw-to-SFM-calibrated detector positions in focal plane coordinates).  Also apparent is an effect from the differential chromatic refraction that is included in the models (and not yet corrected for in the pipelines, though work on this front is in progress).  This is all good news as it indicates that the astrometric fitter is doing its job very well and, from another angle, there is good promise that we will be able to calibrate these effects out with future efforts (and this analysis will provide some validation of such calibrations).

Finally, the following is the version of the astrometry offset std vs. mean for the (now complete) full DP0.2 processing;

.. figure:: /_static/astrometryPlots/astromDistMeanVsStd_DP0p2_rc2_vs_rc5.png
   :width: 500
   :name: fig-astrom-distance-std-vs-mean-dp02

Standard deviation versus mean on-sky distance between reference and matched sources for SFP astrometric calibration for the full DP0.2 processing run (:math:`N_\mathrm{visit} = 19852`, :math:`N_\mathrm{detector} = 2804994`).

Please refer to :ref:`section-sfm-dp0p2-vv` for further visualizations of the full DP0.2 SFP processing results.
