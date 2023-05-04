# Dynamic Systems

A sandbox project for implementing control system algorithms on c++.

# CMake Quickref

This project uses CMake. 

### Generating the Build Files

When freshly setting up the project, generate the build files either by using the `CMake: Configure` command from the CMake Tools extension in VSCode (ctl+shift+p) or by running the cmake command from the commandline within the build directory, i.e.
```
  mkdir build
  cd build
  cmake -G "[Unix Makefiles | Ninja]" ..
```
> To change which generator to use with the CMake Tools extension, go to the settings and change the generator for CMake Tools (serach for 'generator').

### Building the Project

Next, build the project either by using the `CMake: Build` command from the CMake Tools extension or by running `make` or `ninja` from the commandline within the build directory. For multi-core build, use the flag `-j 4`.

> When using the VSCode command palette, you may skip the configuration step and directly use the build command. 

> If the project structure does not change (i.e. only file contents have been modified), there is no need to generate the build files again and you can directly use the build command.

### Running the Application

Run the application from the commandline using `./build/path/to/application`.

### Further Resources:

- `cmake -DCMAKE_BUILD_TYPE=[Debug | Release] ..` to configure the project for debugging or release
- `cmake -DVARIABLE_NAME=value` to set the value of a cmake variable
- `set(VARIABLE_NAME default_value CACHE TYPE "Variable Description")` to declare and cache variable (omit CACHE to only set the variable without caching it).
- `option(OPTION_NAME "description" [ON | OFF])` to add a cached bool variable which are intended for an external user to set (without breaking the build). usually the default value is OFF.
- `message([STATUS ]"Message")` To print a message during configuration
- `ccmake` commandline interface for setting cached variables