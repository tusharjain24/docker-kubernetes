# Key Concepts

## Image
- A docker Image is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, a runtime, system tools, system libraries, environment variables, and configuration files.

- Properties of Image
    1. **Layered**: Images are built up from a series of layers.
    2. **Immutable**: Once an image is created, it cannot be changed. You have to create a new version of the image to make changes.
    3. **Portable**: Images are small in size and can be easily shared and distributed.
    4. **Versioned**: Images can have multiple versions.
    5. **Tagged**: Images can be tagged to make them easier to identify.
    6. **Registry**: Images are stored in a registry.
    
## Container
- A docker Container is a runtime instance of an image. It is a lightweight, standalone, executable package that includes everything needed to run a piece of software.

- Properties of Container
    1. **Isolated**: Containers are isolated from each other.
    2. **Portable**: Containers are small in size and can be easily shared and distributed.
    3. **Versioned**: Containers can have multiple versions.
    4. **Tagged**: Containers can be tagged to make them easier to identify.
    5. **Registry**: Containers are stored in a registry.
    