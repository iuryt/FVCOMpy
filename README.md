

<!-- Title -->
<h1 align="center">
  FVCOMpy
</h1>

<!-- description -->
<p align="center">
  <strong> Reading and regriding FVCOM outputs with Python <a href="https://docs.xarray.dev/en/stable/">xarray</a>.</strong>
</p>

 
<p align="center">
  <img src="https://github.com/iuryt/FVCOMpy/blob/main/img/fvcom_grid.png" /></br>
  Source: <a href="https://tos.org/oceanography/assets/docs/19-1_chen.pdf">Advances in Computational Oceanography</a>
</p>


**FVCOM** stands for Finite-Volume Coastal Ocean Model. This model uses an unique _unstructured grid_ that allows easily to setup focus points without having to nest different meshes. One of the only drawbacks is that the unstructured grid turns very difficult to _offline_ analyses. The model output also commonly use the same name for coordinates and dimensions. For instance, the model has sigma layers coordinate `siglay` that depends on `(siglay,node)`, crashing with `xarray` notion of coordinates (see discussion in [xarray #2233](https://github.com/pydata/xarray/issues/2233))

One of the main reason to create this repository is to _investigate alternatives_ for users to use FVCOM outputs in their researches, e.g. the [Northeast Coastal Ocean Forecast System (**NECOFS**)](http://fvcom.smast.umassd.edu/necofs/). The starting point is to create some tutorial notebooks showing solutions for reading and regriding FVCOM data to allow using `xarray` for multidimensional analysis. With time, we could try to wrap it as a `Python` package.

<p align="center">
  NECOFS data
  <img src="https://github.com/iuryt/FVCOMpy/blob/main/img/scatter_temperature_salinity.png" /></br>
</p>

## Currently available tutorials

| Tutorial    | Badge       |
| ----------- | ----------- |
| 00-Getting Started      | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/iuryt/FVCOMpy/blob/main/examples/00-GettingStarted.ipynb)      |
