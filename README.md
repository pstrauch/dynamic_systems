# Dynamic Systems

A sandbox project for implementing control system algorithms on c++.

# CMake Quickref

This project uses CMake. 

### Generating the Build Files

When freshly setting up the project, generate the build files either by using the `CMake: Configure` command from the VSCode command palette (ctl+shift+p) or by running the cmake command from the commandline within the build directory, i.e.
```
  mkdir build
  cd build
  cmake ..
```

### Building the Project

Next, build the project either by using the `CMake: Build` command from the VSCode command palette or by running the `make` command from the commandline within the build directory. For multi-core build, use the flag `make -j 4`.

> When using the VSCode command palette, you may skip the configuration step and directly use the build command. 

> If the project structure does not change (i.e. only file contents have been modified), there is no need to generate the makefiles again and you can directly use the build command.

### Running the Application

Run the application from the commandline using `./build/path/to/application`.

### Further Resources:

`ccmake` command-line-interface for setting compiler flags