# CPP Template Conan

A C++ Template using conan package manager

## Set up conan

The conan example is taken from <https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html>.

1. Detect conan profile

    ```bash
    conan profile detect --force
    ```

    The conan profile will be stored under `/Users/<user>/.conan2/profiles/default`.

- Build Release

    1. Install conan packages

        ```bash
        conan install . --output-folder=build --build=missing
        ```

    2. Build project using CMake

        ```bash
        cmake --preset conan-release
        ```

- Build Debug

    1. Install conan packages

        ```bash
        conan install . -s build_type=Debug --output-folder=build --build=missing
        ```

    2. Build project using CMake

        ```bash
        cmake --preset conan-debug
        ```
