dockerfeed
==========

Create a docker build context and augment it with a replacement Dockerfile or other content added

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
