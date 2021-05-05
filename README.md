# OMS_Project_WHETGEO1D


# Website
- [GEOframe](http://geoframe.blogspot.com/)
- [Object Modeling Sytem (OMS)](https://alm.engr.colostate.edu/cb/project/oms)

# OMS
`WHETGEO1D` is written in Java,  works under the [`OMS3`](https://abouthydrology.blogspot.com/2017/08/oms-3-essentials.html)(David et al., 2013) framework and it is part of the `GEOframe` system ([Formetta et al., 2014](https://doi.org/10.1016/j.envsoft.2014.01.019), [Bancheri, 2017](http://eprints-phd.biblio.unitn.it/2679/)). It was produced as part of the Ph.D. work by Niccolò Tubini.
Here you can find the [source code](https://github.com/geoframecomponents/WHETGEO-1D)

GEOframe programs run on Java 8. The OMS project can be run either within the OMS v3 Console or by using [Docker](https://hub.docker.com/r/omslab/oms/).

## OMS v3 Console
- As first step it is necessary to install the JDK 8. There are two options:
  - Download open JDK 8 LTS from https://adoptopenjdk.net/
    - Install it
    - find the JAVA_HOME
      - on Windows open a terminal and run `where javac`
      - on Mac open a terminal and run `where java`
  or
  - install Anaconda
    - create the environment geoframe_vicenza. This install a JDK 8 on your laptop. To create an enviroment open the Anaconda prompt
    - open Anaconda prompt
      - set in the folder containing the file *geoframe_vicenza.yaml*
      -  `conda env create -f geoframe_vicenza.yaml`
      -  `conda activate geoframe_vicenza`
    - find the JAVA_HOME
      - from the Anaconda prompt `echo JAVA_HOME`
    
- Download the OMS v3 Console version 3.6.28 from  https://alm.engr.colostate.edu/cb/wiki/16961
- Unzip the OMS Console and 
  - on Windows run the `console.bat` file
  - on Mac or Linux open a terminal and execute `./console.sh &`

- In the console setting, select the panel Run and set the Java path to the previously installed JDK. The Java path can be  
![Alt text](Documentation/Figures/java_path.png?raw=true "Title")

## OMS from Docker
Please refers to the guidelines at https://hub.docker.com/r/omslab/oms/. Please use the version `0.3_py3`.

# Project documentation
In the folder `Documentation` you can find
- `_README.ipynb` containing a description of the folder structure;
- `00_How_to_Read_NetCDF.ipynb` containing a brief introduction to [NetCDF](https://www.unidata.ucar.edu/software/netcdf/docs/index.html) and the Python library [xarray](http://xarray.pydata.org/en/stable/index.html);
- `00_OMS_Timeseries.ipynb` showing the structure of a .csv file OMS compliant and how to prepare timeseries input;
- `00_Richards_computational_grid.ipynb` containing a detailed descritption of how to prepare the input file to define the computational grid;
- `00_WHETGEO1D_Richards.ipynb` containing the documentation to setup the .sim file to solve the Richards' equation.

# Acknowledgements

-  Niccolò Tubini, Riccardo Rigon developed the theoretical aspects of the model (Authors). 
-  Niccolò Tubini, Riccardo Rigon designed the first version of the code (Authors)
-  Niccolò Tubini implemented and deployed it (Authors)
-  Riccardo Rigon provided financial support
-  Niccolò Tubini and Riccardo Rigon wrote the documentation in the Notebooks
-  Niccolò Tubini was supported by a Ph.D. grant by [DICAM-UniTrento](https://www.unitn.it/dricam/) and by the PRIN 2017 project [WATZON (WATer mixing in the critical ZONe: observations and predictions under environmental changes)](http://abouthydrology.blogspot.com/2019/06/the-watzon-project.html).
-  We thank Professor Vincenzo Casulli and Professor Michael Dumbser for their fruitful discussions on the numerical aspects of the work. 
