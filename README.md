# geoviews-geopython-2018

Material for my talk "Approaching geovisualization and remote sensing with GeoViews" @ [GeoPython 2018](http://2018.geopython.net/).

![Basel Parks and Cafes](https://github.com/jackdbd/geoviews-geopython-2018/blob/master/screenshots/basel_parks_and_cafes.png "A Screenshot of this application, showing Basel Parks and Cafes.")


## Installation

The best way to install all the dependencies for this notebook is to create a conda environment. Either [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://repo.continuum.io/) are good.

You can use the `freeze.yml` file included in this repository to create a conda environment identical to the one I used:

```shell
conda env create --file freeze.yml
```

Otherwise you can create and activate a new conda environment with:

```shell
conda create --name geopython-2018 python=3.6 --yes
source activate geopython-2018
```

And install all the dependencies with:

```shell
# geoviews (it depends on holoviews)
conda install -c conda-forge -c ioam holoviews geoviews --yes
# Additional packages (for the examples in the notebook)
conda install xarray  -y
conda install -c conda-forge iris -y
conda install -c conda-forge iris-sample-data
conda install -c conda-forge geopands -y
```

You will also need to download the Bokeh sample data:

```
import bokeh.sampledata
bokeh.sampledata.download()
```

If you run into issues when importing `geopandas`, try manually downgrading `fiona`:

```
conda install -c conda forge fiona=1.7.10
```


## Data

In order to run the notebook you will also need some data files.

Here is where to find the data used in the notebook:

- Shapefiles of Basel @ https://extract.bbbike.org/
- netCDF file (Air quality) @ [NOAA](https://www.esrl.noaa.gov/psd/repository/entry/show?entryid=synth%3Ae570c8f9-ec09-4e89-93b4-babd5651e7a9%3AL25jZXAucmVhbmFseXNpcy5kZXJpdmVkL3N1cmZhY2UvYWlyLm1vbi5tZWFuLm5j)
- Shapefile of American Indian/Alaska Native Areas/Hawaiian Home Lands @ [United States Censun Bureau](https://www.census.gov/geo/maps-data/data/cbf/cbf_aiannh.html)

Create a `data` directory in the root of the repository and drop the files there.


## Other

You could freeze your environment with:

```shell
conda env export > freeze.yml
```

To remove this conda environment, run:

```shell
conda env remove -n geopython-2018
```
