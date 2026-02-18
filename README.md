# CST8915 Lab4

## Demo Video

Demo Video link: https://www.youtube.com/watch?v=Hyf5Q5d3v0A

## Reflection Questions

### What are the main differences between a Docker image and a Docker container?

A Docker image is a read-only template that contains everything needed to run an application, including the code, runtime, libraries, and dependencies. A Docker container is a running instance of that image. In other words, an image is like a blueprint, and a container is the actual running application built from that blueprint. So the main difference is that an image is static and reusable, while containers are dynamic: can be started, stopped, or deleted without affecting the original image.

## Explain how Docker's layered architecture improves efficiency

Each instruction in a Dockerfile creates a new layer. These layers are cached and reused across images, which means Docker does not need to rebuild or re-download everything when only small changes are made. This improves build speed, reduces storage usage, and allows multiple containers to share the same base layers in memory. As a result, Docker images are lightweight and efficient.

## Why does each container get its own writable layer?

Each container gets its own writable layer so it can modify files and store runtime data without changing the original image or affecting other containers. If a container is deleted, only its writable layer is removed, while the shared image layers remain unchanged and reusable.

## What are the benefits of using Docker Compose over running containers individually?

Docker Compose makes it easier to run applications that use multiple containers by letting you define everything in one configuration file. Instead of running many docker run commands manually, you can start, stop, or rebuild all containers using a single command. It also automatically handles networking and storage between containers, which helps avoid setup mistakes and keeps environments consistent.
