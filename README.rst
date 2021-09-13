cf-xarray-earthcube
###################

.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.5496371.svg
   :target: https://doi.org/10.5281/zenodo.5496371

Interactive notebook: |binder|

**cf-xarray: Scale your analysis across datasets with less data wrangling and more metadata handling**

**Authors:** Deepak Cherian, Mattia Almansi, Pascal Bourgault

There has been an explosion in the availability of terabyte to petabyte-scale geoscience datasets, particularly on the cloud, prompting the development of scalable tools and workflows to handle such big datasets by Earthcube projects such as Pangeo. There is a parallel need for tools that enable the analysis of datasets from a wide variety of sources that each have their own nomenclature.

Xarray is a python package that enables easy and convenient labelled data analytics by allowing users to leverage metadata such as dimension names and coordinate labels. cf-xarray is an open-source      Apache licensed Xarray extension that decodes Climate and Forecast (CF) Metadata conventions adopted by the geoscience community, allowing users to extensively use standardized metadata such as          “standard names” in their analysis pipelines. For example, the zonal average of an Xarray dataset `ds` is seamlessly calculated as ``ds.cf.mean("longitude")`` on a wide variety of CF-compliant datasets, regardless of the actual name of the “longitude” variable (e.g. “lon”, “lon_rho”, “long”). cf-xarray also provides tools and heuristics to optionally guess absent attributes, allowing usage on           incompletely tagged datasets.  cf-xarray is now seeing adoption in other packages such as xESMF, a package for regridding of Xarray datasets; and NOAA’s Model Diagnostic Task Force (MDTF) diagnostic     workflow for validating model simulations.

Our notebook will demonstrate the use of cf-xarray to build an analysis pipeline that works on a wide variety of cloud-available datasets such as the CMIP6 archive, the CESM Large Ensemble, various      satellite datasets, and that uses xESMF to regrid this wide variety of datasets to a common grid to facilitate analysis of anomalies.

.. |binder| image:: https://binder.pangeo.io/badge_logo.svg
   :alt: binder
   :target: https://binder.pangeo.io/v2/gh/earthcube2021/ec21_cherian_etal/main?filepath=DC_01_cf-xarray.ipynb
