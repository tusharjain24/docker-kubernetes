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

## Multi-Stage Build
- Multi-Stage Build is a build process that uses multiple stages to build an image. It helps in :
    1. Reducing the size of the image.
    2. Improving the security of the image.
    3. Improving the performance of the image.
    4. Cleaner Production container

```dockerfile
# Build stage
FROM node:22-alpine AS builder
WORKDIR /app
COPY package`*.json ./
RUN npm install
COPY . .
RUN npm run build

# Runtime stage
FROM node:22-alpine
WORKDIR /app`
COPY --from=builder /app/dist ./dist
COPY package*.json ./
RUN npm install --only=production
CMD ["node", "dist/index.js"]
```

## Container Networking(Network Drivers)
- Container networking is the process of connecting containers to a network. It is used to enable communication between containers and other networked devices.

- `COMMAND` : docker network 

- Types of Network Drivers(Network Types):
    1. `Bridge` (Default): Containers on the same host can communicate with each other, external access needs port mapping.
    2. `Host`: The container shares the host's network namespace (no isolation).
    3. `None`: The container has no network namespace ( completely isolated).
    4. `Overlay`: Enables multi-host networking for Swarm services.
    5. `Macvlan`: Assigns a MAC address to the container (acts like a physical device) and allows it to communicate with other devices on the network.
    6. `Ipvlan`: Assigns an IP address to the container (acts like a physical device) and allows it to communicate with other devices on the network. (Not used much)


    