# geoviews-geopython-2018

Material for my talk "Approaching geovisualization and remote sensing with GeoViews" @ [GeoPython 2018](http://2018.geopython.net/).

![Basel Parks and Cafes](https://github.com/jackdbd/geoviews-geopython-2018/blob/master/screenshots/basel_parks_and_cafes.png "A Screenshot of this application, showing Basel Parks and Cafes.")


## Installation

The best way to install all the dependencies for this notebook is to create a conda environment.

You can use the `freeze.yml` file to create an identical environment I used:

```shell
conda env create --file freeze.yml
```

Otherwise you can create and activate a new conda environment with:

```shell
conda create --name geopython-2018 python=3.6
source activate geopython-2018
```

And install all dependencies with:

```shell
conda install -c conda-forge -c ioam holoviews geoviews
conda install xarray
conda install -c conda-forge iris
```


## Data

Create a `data` directory in the root of the repository and drop the files there.

Here is where to find the data used in the notebook:

- Shapefiles of Basel @ https://extract.bbbike.org/
- netCDF file (Air quality) @ [NOAA](https://www.esrl.noaa.gov/psd/repository/entry/show?entryid=synth%3Ae570c8f9-ec09-4e89-93b4-babd5651e7a9%3AL25jZXAucmVhbmFseXNpcy5kZXJpdmVkL3N1cmZhY2UvYWlyLm1vbi5tZWFuLm5j)
- Shapefile of American Indian/Alaska Native Areas/Hawaiian Home Lands @ [United States Censun Bureau](https://www.census.gov/geo/maps-data/data/cbf/cbf_aiannh.html)


## Other

You could freeze your environment with:

```shell
conda env export > freeze.yml
```

To remove this conda environment, run:

```shell
conda env remove -n geopython-2018
```
