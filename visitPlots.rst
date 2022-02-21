Visit Plots
===========

Initial Data
------------
Initially the data in a number of precursor collections was studied while the
plots were being developed. During this investigation an offset in the
photometry was found as shown in the Figure below. This was then corrected for
in the later processing.

.. figure:: _static/scatterPlotVisit_CircAp12_sub_PS_meas_scatter_HSC_i_HSC-I_1228_hsc_rings_v1_u_sr525_visitPlots_20211112T023306Z.png
    :name: magOffset
    :target: _images/scatterPlotVisit_CircAp12_sub_PS_meas_scatter_HSC_i_HSC-I_1228_hsc_rings_v1_u_sr525_visitPlots_20211112T023306Z.png
    :alt: This plot shows the magnitude offset for HSC data, while this is not
          the DP0 data it was processed with the same pipeline and shares the same
          issues.

    This plot shows the magnitude offset for HSC data, while this is not the DP0
    data it was processed with the same pipeline and shares the same issues.

This issue was fixed before the main processing began.

Large Scale Processing
----------------------
Once the initial data had been studied the large scale processing started.
Plots were made of this data at the visit level. Plots for one, representative,
visit are included here.

.. figure:: _static/scatterPlot_CircAp12-PS_all.png
    :name: scatterPlot_CircAp12-PS_all
    :target: _images/scatterPlot_CircAp12-PS_all.png
    :alt: The magnitude for a 12 pixel circular aperture - the PSF magntiude
          for stars and galaxies.

    The magnitude for a 12 pixel circular aperture - the PSF magntiude
    for stars and galaxies.

.. figure:: _static/scatterPlot_CircAp12-PS_gals.png
    :name: scatterPlot_CircAp12-PS_gals
    :target: _images/scatterPlot_CircAp12-PS_gals.png
    :alt: The magnitude for a 12 pixel circular aperture - the PSF magnitude
          for just the galaxies.

    The magnitude for a 12 pixel circular aperture - the PSF magnitude for just
    galaxies.

.. figure:: _static/scatterPlot_CircAp12-PS_meas_calibPsfUsed.png
    :name: scatterPlot_CircAp12-PS_meas_calibPSfUSed
    :target: _images/scatterPlot_CircAp12-PS_meas_calibPsfUsed.png
    :alt: The magnitude for a 12 pixel circular aperture - the PSF magntiude
          for stars that were used as calibration sources for the PSF.

    The magnitude for a 12 pixel circular aperture - the PSF magntiude
    for stars that were used as calibration sources for the PSF.

.. figure:: _static/scatterPlot_CircAp12-PS.png
    :name: scatterPlot_CircAp12-PS
    :target: _images/scatterPlot_CircAp12-PS.png
    :alt: The magnitude for a 12 pixel circular aperture - the PSF magntiude
          for stars.

    The magnitude for a 12 pixel circular aperture - the PSF magntiude
    for stars.

.. figure:: _static/scatterPlot_CircAp25-PS_all.png
    :name: scatterPlot_CircAp25-PS_all
    :target: _images/scatterPlot_CircAp25-PS_all.png
    :alt: The magnitude for a 25 pixel circular aperture - the PSF magntiude
          for stars and galaxies.

    The magnitude for a 25 pixel circular aperture - the PSF magntiude
    for stars and galaxies.

.. figure:: _static/scatterPlot_CircAp25-PS_gals.png
    :name: scatterPlot_CircAp25-PS_gals
    :target: _images/scatterPlot_CircAp25-PS_gals.png
    :alt: The magnitude for a 25 pixel circular aperture - the PSF magntiude
          for galaxies.

    The magnitude for a 25 pixel circular aperture - the PSF magntiude
    for galaxies.

.. figure:: _static/scatterPlot_CircAp25-PS_meas.png
    :name: scatterPlot_CircAp25-PS_meas
    :target: _images/scatterPlot_CircAp25-PS_meas.png
    :alt: The magnitude for a 25 pixel circular aperture - the PSF magntiude
          for stars.

    The magnitude for a 25 pixel circular aperture - the PSF magntiude
    for stars.

.. figure:: _static/skyPlot_CircAp12-PS_measGals.png
    :name: skyPlot_CircAp12-PS_measGals
    :target: _images/skyPlot_CircAp12-PS_measGals.png
    :alt: The sky distribution of the magnitude for a 12 pixel aperture - the
          PSF magnitude for galaxies.

    The sky distribution of the magnitude for a 12 pixel aperture - the
    PSF magnitude for galaxies.

.. figure:: _static/skyPlot_CircAp12-PS_measStars_calibPsfUsed.png
    :name: skyPlot_CircAp12-PS_measStars_calibPsfUsed
    :target: _images/skyPlot_CircAp12-PS_measStars_calibPsfUsed.png
    :alt: The sky distribution of the magnitude for a 12 pixel aperture - the
          PSF magnitude for stars used as PSF calibration sources.

    The sky distribution of the magnitude for a 12 pixel aperture - the PSF
    magnitude for stars used as PSF calibration sources.

.. figure:: _static/skyPlot_CircAp12-PS_measStars.png
    :name: skyPlot_CircAp12-PS_measStars
    :target: _images/skyPlot_CircAp12-PS_measStars.png
    :alt: The sky distribution of the magnitude for a 12 pixel aperture - the
          PSF magnitude for stars.

    The sky distribution of the magnitude for a 12 pixel aperture - the PSF
    magnitude for stars.

.. figure:: _static/skyPlot_PSFluxSN.png
    :name: skyPlot_PSFluxSN
    :target: _images/skyPlot_PSFluxSN.png
    :alt: The sky distribution of the PSF flux SN for all sources.

    The sky distribution of the PSF flux SN for all sources.

.. figure:: _static/skyPlot_skyObject.png
    :name: skyPlot_skyObject
    :target: _images/skyPlot_skyObject.png
    :alt: The sky distribution of the sky object fluxes.

    The sky distribution of the sky object fluxes.

This plots show that the offset seen before has been fixed and don't show up
any other obvious issues. Plots studying the ellipticity were also made and
some examples are given below.

.. figure:: _static/skyPlot_E2_stars.png
    :name: skyPlot_E2Psf_stars
    :target: _images/skyPlot_E2_stars.png
    :alt: The sky distribution of E2 (2ixy/(ixx + iyy)) calculated for the PSF.

    The sky distribution of E2 (2ixy/(ixx + iyy)) calculated for the PSF.

.. figure:: _static/scatterPlot_E2_stars.png
    :name: scatterPlot_E2_stars
    :target: _images/scatterPlot_E2_stars.png
    :alt: A scatter plot of E2 (2ixy/(ixx + iyy)) calculated for the CModel
          shape.

    A scatter plot of E2 (2ixy/(ixx + iyy)) calculated for the CModel shape.

More plots are available for a variety of visits and can be viewed through the
plot viewer in the u/sr525 collections.
