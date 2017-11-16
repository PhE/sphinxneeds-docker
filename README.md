# SPHINX Quickstart

container to generate SPHINXneeds documentation. Will output HTML and PDF

Build the container with:

```
    docker build -t sphinxneeds_image .
```
the input folder should contain the project documentation.

The output folder should be empty. Existing content may be overwritten!

Run the container with

```
    docker run --name sphinxneeds --rm \
    -e "Project=Sphinx in a docker" \
    -e "Author=Till Witt" \
    -e "Version=v1.0" \
    -v "$(pwd)/input:/project/input" \
    -v "$(pwd)/output:/project/output" \
        -i -t sphinxneeds_image
```
