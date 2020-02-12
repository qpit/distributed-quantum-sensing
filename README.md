# Data analysis for Distributed quantum sensing in a continuous-variable entangled network

This notebook accompanies the paper [X. Guo, C. R. Breum, J. Borregaard, S. Izumi, M. V. Larsen, T. Gehring, M. Christandl, J. S. Neergaard-Nielsen & U. L. Andersen, _Distributed quantum sensing in a continuous-variable entangled network_, Nature Physics (2019)](https://doi.org/10.1038/s41567-019-0743-x). 
It demonstrates how to get from the phase calibration data and the raw oscilloscope trace measurements to the main results of the study, presented in Figure 3 of the paper.

To run the notebook, the following data files must be present in the same folder:

* `distsens_phasecalibration.hdf5`
* `distsens_spectra.hdf5` and/or `distsens_raw.hdf5`

`distsens_raw.hdf5` contains the raw oscilloscope traces and is 7.7 GB large. The initial processing of these data consists of normalization among the four channels and computation of the averaged power spectral densities (across 2000 traces) along with their variances. It is possible to skip these steps and simply load the already processed spectra contained in `distsens_spectra.hdf5`.

The data files are available from the DTU Data repository: https://doi.org/10.11583/DTU.9988805

Furthermore, the following Python packages are required:

* [NumPy](https://numpy.org/)
* [SciPy](https://scipy.org/scipylib/)
* [matplotlib](https://matplotlib.org)
* [h5py](https://www.h5py.org/)
* [Jupyter lab or notebook](https://jupyter.org/)
