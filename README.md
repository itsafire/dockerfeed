dockerfeed
==========

Create a docker build context and augment it with a replacement Dockerfile or other content added.

If you are in need of building a docker image with a different Dockerfile, you have to replace the Dockerfile
in the filesystem. It is not possible to tell docker to use a different Dockerfile. If you don't want to alter
the sources of your build, you can take advantage of using the tar input of `docker build`. With the help of
`dockerfeed` you are able to control which Dockerfile will be used for the build. Addionally you can insert
additional paths into the docker build context.

A build could look like this:

```
dockerfeed -d ../Dockerfile.special path/to/dockerimagesource | docker build -t myspecialimage -
``` 

```
usage: dockerfeed [-h] [-p PATH] [-d DOCKERFILE] context

Replace Dockerfile and/or replace file path in context

positional arguments:
  context               path to context

optional arguments:
  -h, --help            show this help message and exit
  -p PATH, --path PATH  path to add/override in context. example:
                        /path/to/./path_to_be_inserted
  -d DOCKERFILE, --dockerfile DOCKERFILE
                        replacement dockerfile
  ```
