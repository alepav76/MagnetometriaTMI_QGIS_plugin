Overview

TMI Magnetometric Processing is a specialized QGIS plugin designed for geophysicists, exploration geologists, and GIS professionals working with aeromagnetic or ground magnetic survey data. It automates the calculation of essential magnetic derivatives and gradient enhancements from Total Magnetic Intensity (TMI) raster grids.

Key Features

Horizontal Derivatives ($\partial T / \partial x$, $\partial T / \partial y$): Computed using robust gradient operators aligned with the dataset's coordinate system.
Vertical Derivative via 2D FFT: Evaluates the first vertical derivative in the spectral domain using the wavenumber filter ($\vert{}k\vert{} = 2\pi\sqrt{FX^2 + FY^2}$), incorporating mirrored padding to minimize boundary artifacts.
Horizontal Gradient Amplitude ($GH$): Combines orthogonal horizontal gradients to highlight structural lineaments and contact boundaries.
Analytic Signal Amplitude ($AS$): Calculates the total analytic signal to map magnetic source locations independently of the geomagnetic inclination and declination.
Data Integrity & Masking: Automatically handles NoData values using Euclidean distance transforms for temporary filling, applying robust edge-masking to prevent border-effect propagation.
Integrated Reporting: Generates a comprehensive technical text report containing statistical summaries, processing parameters, and grid metadata.Seamless QGIS Integration: Automatically validates projected CRS units, checks for grid rotation/shear, and optionally loads all derived products directly into the active QGIS project.

System Requirements

Compatibility: QGIS 3.44.x / Python 3.12
Dependencies: numpy, scipy, GDAL (bundled with QGIS)
Input Requirements: Regular grid raster (GeoTIFF, VRT, IMG, ASC) in a projected CRS with linear units (preferably meters).

Note: This plugin was developed with the assistance of AI.
