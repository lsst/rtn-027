.. _section-sfm-dp0p2-vv:
Single Frame Processing: Full DP0.2 Summary
==========================================

The following provides an overview summary of the visit-level (Single Frame Processing) results from the full DP0.2 processing (see `PREOPS-905 <https://jira.lsstcorp.org/browse/PREOPS-905>`__ for details of the processing).  For reference, this includes 19852 individual visits comprising 2,804,994 successfully proceseed detetector ids.

Parameter correlations from visitSummary Tables
-----------------------------------------------

The visitSummary data products provide summaries of various detector-level quantities derived from the SFP. In this section we provide various visualizations of the quantities provided as a function of band and posittion (in both Focal Plan and sky coordinates.  See Jira ticket `PREOPS-849 <https://jira.lsstcorp.org/browse/PREOPS-849>`__ for further details.

The following shows some correlations between various parameters.


.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_visitSummary_DP0.2_v23.png
   :name: fig-DP0p2-visitSummary
Standard deviation versus mean on-sky distance between reference and matched sources for SFP astrometric calibration. Left: pre-thresholding.  Right: post-thresholding.


Visit/detector quantities as a funtion of position on the focal plane
---------------------------------------------------------------------

The following plots various parameters as a function of position in the focal plane and per band:

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_visitSummary_focalPlane_DP0.2_v23.png
   :name: fig-DP0p2-visitSummary_focalPlane

Distribution of the mean astrometry distance as a function of position in the focal plane.  Each visit/detector gets a single point and, for visualization purposes, the position each point is staggered within the detector boundaries.

No trend with position on the focal plane is observed.

Visit/detector quantities as a funtion of position on the sky
-------------------------------------------------------------

The following plots various parameters as a function of position in the focal plane and per band:

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_visitSummary_raDec_DP0.2_v23.png
   :name: fig-DP0p2-visitSummary_raDec

Distribution of various visit/detector-level quantities as a function of position on the sky.

Histogram distributions of visit/detector quantities per band
-------------------------------------------------------------

The following plot various parameters distributions for the visit/detector DP0.2 SFP sample.

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_astromOffsetMean_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_astromOffsetMean

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_astromOffsetStd_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_astromOffsetStd

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_psfSigma_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_psfSigma

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_medianE_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_medianE

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_psfStarScaledDeltaSizeScatter_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_psfStarScaledDeltaSizeScatter

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_skyBg_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_skyBg

.. figure:: /_static/fullDP0p2SfpSummaryPlots/LSSTCam-imSim_VisitSummaryDistributions_zeroPoint_DP0.2_v23_log_bin100.png
   :width: 700
   :name: fig-DP0p2-visitDistributioins_zeroPoint
