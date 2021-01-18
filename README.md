# alpine-iso
A set of Alpine Docker images... containing their respective Alpine ISO

DockerHub: https://hub.docker.com/repository/docker/raonigabriel/alpine-iso

The ideas behind this GitHub repository are:
1. Use the GitHub Actions [Build Matrix](https://proandroiddev.com/how-to-github-actions-build-matrix-e6a1433a8ff5) combined with sub-folders to have **sub-modules** within the repo. 
2. Use the GitHub Actions [Manual Triggers](https://github.blog/changelog/2020-07-06-github-actions-manual-triggers-with-workflow_dispatch/) with inputs (params).
3. Use [symlinks](https://mokacoding.com/blog/symliks-in-git/) within the repo (**./virt**/Dockerfile, **./extended**/Dockerfile and **./xen**/Dockerfile are symlinks to **./standard**/Dockerfile).
4. How to use an **ARG** before the **FROM** [instruction](https://blog.bitsrc.io/how-to-pass-environment-info-during-docker-builds-1f7c5566dd0e).
5. Introduce the **/etc/os-release** file (found on the base Alpine image) so that we can take advandage of it by using the [source](https://linuxize.com/post/bash-source-command/) command.
6. Demonstrate that we can use Docker images for the sole purpose of storing **big ISO** files. 😬

## Features
Each image variant is build from the respective Docker image and contains its corresponding ISO image on **/**.  
The **all** variant contains all the 4 ISO files.

## Tags (based on [x64 Alpine ISOs](https://www.alpinelinux.org/downloads/) available for download)
* raonigabriel/alpine-iso:standard-x.y.z
* raonigabriel/alpine-iso:extended-x.y.z
* raonigabriel/alpine-iso:virt-x.y.z
* raonigabriel/alpine-iso:xen-x.y.z
* raonigabriel/alpine-iso:all-x.y.z

Where x.y.z above is a valid Alpine release version, eg. 3.13.0

## Simple usage (you can bind mount to 'retrieve' the ISO)

```sh
# docker run --rm -it raonigabriel/alpine-iso:standard-3.13.0
# ls -la *.iso
# -rw-r--r--    1 root     root     139460608 Jan 18 19:41 alpine-standard-3.13.0-x86_64.iso
```