#############
testdata_rail
#############

``testdata_rail`` provides a minimum amount of test data sufficient to run the LSST Science Pipelines `meaz_pz`_ for HSC, DC2 and ComCam datasets.

.. _meas_pz: https://github.com/lsst-dm/meas_pz

Contents of this package
========================

A clone of this package will take about 1.2GB of disk space: about 800GB of ML Models, 400MB of object files, and their git LFS copies.

data files
----------

The ``data/`` directory contains 3 object files.


models
------

The ``models/`` directory contains files for ML models.


Running the tests
=================

Set up the package
------------------

This package provides the test data for the `ci_hsc`_ package: both this and `ci_hsc`_ must be setup in eups in order to run the tests in `ci_hsc`_.
One way to accomplish this is as follows::

  $ cd testdata_rail
  $ setup -r .
  $ cd PATH_TO_MEAS_PZ
  $ setup -kr .
  $ py.test

git lfs
=======

The data used by ``meas_pz`` is stored using `Git LFS`_; refer to the `relevant LSST documentation`_ for details on how to check out this repository.

.. _Git LFS: https://git-lfs.github.com
.. _relevant LSST documentation: http://developer.lsst.io/en/latest/tools/git_lfs.html
