# CPP Template Conan

A C++ Template using conan package manager

## Set up conan

The conan example is taken from <https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html>.

1. Detect conan profile

    ```bash
    conan profile detect --force
    ```

    The conan profile will be stored under `/Users/<user>/.conan2/profiles/default`.

2. Install conan packages

    ```bash
    conan install . --output-folder=build --build=missing
    ```

3. Build project using CMake

    ```bash
    cmake --preset conan-release
    ```

## Open Questions

1. What does `CMakeUserPresets.json` do?
