# NumSim
A flow solver for the Navier-Stokes equations with some nice features such as arbitrary geometries, heat transport and interaction with solids.

## Installation & Prerequisites

You need
- gcc
- libvtk and
- cmake to compile and build this project succesfully.
Execute ``` sudo apt install gcc cmake ``` inside the terminal to install the first two tools. For libvtk enter ``` sudo apt install libvtk``` and press the "tab-key" for autocompletion proposals and choose the version you like.

Executing ``` cd build && cmake .. & make -j && make install ``` in the main project folder compiles the sources and copys the executable to the build directory.
The first time the command above will fail, because there is no build  directory. Simply enter ``` mkdir build ``` to create the directory.

## Usage

- Run the programm: ``` ./numsim ../ini/your_szenario.txt ```

## Visualization

The results of the simulation (velocity u, velocity v, pressure p) will be saved for every timestep in the folder ```/out``` and can be visualized with paraview.

## Documentation
Run ```doxygen ./docs/doxyfile``` in the project folder to create the html and latex documentation. You can access the main page of the html documentation by opening ```docs/html/index.html``` with a browser of your choice.

## Fixes

If you installed libvtk manually and not with ``` sudo apt-get install libvtk ``` maybe you need to export the library path ```export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH```

## Running the tests

``` cd build && cmake .. & make -j && ctest -r ```

## Authors

* **Author 1** - *Initial work* - [kaiserls](https://github.com/kaiserls)

* **Author 2** - *Initial work* - ...

* **Author 3** - *Further work* - ...
