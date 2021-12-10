
Input Data Validation
---------------------

Prior to the start of processing, it was necessary to ensure that all the expected simulated images
were available in the IDF data repository. In the case of real observations, we would expect to
compare the list of observed visits with the data present in the repository, assuming that each
visit should contain data from all sensors in the camera. However, in the case of the DC2
simulations, only sensors that fell inside the target simulation footprint were simulated, which
means that a large fraction of visits are incomplete. As a result, we must compare the total list of
visits with some estimation of which sensors should or should not exist based on this footprint
selection in order to identify any "missing" images.

In doing this comparison, there were approximately 5.9 million potential detector images in the Cartesian
detector x visit product, and of these only 4.2 million actual detector images. The vast majority of
the missing images were outside the survey boundary, but approximately 0.1% were well inside the
footprint (or 0.06% of the simulated images.) The boundaries of some of these individual missing
detectors are shown below.

.. figure:: /_static/missing_raw_ccds.png
   :name: missing_raws

   Outlines of individual detectors that were missing from the DC2 data repository.

Since there was no record of these images at any Rubin computing site, we followed up with DESC
about any potential causes. In some of the early simulation runs there were problems with batch jobs
running out of memory, and some of these jobs were abandoned rather than retried and completed.
Since the logs from these runs are no longer available, and since the number of affected images is
very small, there no further follow-up was necessary.

**Implementation details:** The key step in finding "missing" images is to take the set of (detector,
visit) data ID's that "could" exist, i.e. the Cartesian product of all the visits with all the
detectors, and subtract from that the data IDs that have valid raw images. This looks like:

::

    all_possible_dataIds = set(butler.registry.queryDataIds(("visit", "exposure", "detector"),
                                                            where="instrument='LSSTCam-imSim'"))
    only_extant_dataIds = set(butler.registry.queryDataIds(("visit", "exposure", "detector"),
                                                           where="instrument='LSSTCam-imSim'",
                                                           datasets="raw"))
    missing_raws = list(all_possible_dataIds - only_extant_dataIds)

In the case of the DC2 data, this list of potentially-missing data IDs is then filtered by on-sky
position, leaving only detectors that fell well within the simulation boundary.

