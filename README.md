# gltf2glb
GLTF to Binary GLTF (GLB) Converter

Created by Christopher Mitchell, Ph.D. et alia of Geopipe, Inc.

This project was inspired by https://github.com/Qantas94Heavy/binary-gltf-utils and started as a direct Javascript-to-Python port with a bunch of bugfixes. It implements `b3dm` headers for Cesium 3D Tiles, and will soon implement `i3dm` as well. It also includes a `packcmpt` tool for combining one or more `i3dm`/`b3dm` models into a single `cmpt` file.

Usage
-----

### gltf2glb ###
    ./gltf2glb.py [-e|--embed] [-c|--cesium] [-i|--i3dm instance_table] [-b|--b3dm batch_table] input_file

`-e|--embed`: Embed shaders and textures in the GLB file, even if not already embedded.

`-c|--cesium`: [DEPRECATED] Use the binary buffer name `KHR_binary_glTF`. Cesium no longer requires this.

`-i|--i3dm`: Export i3dm, with optional path to JSON instance table data. Use "" for the path if there's no instance data to include.

`-b|--b3dm`: Export b3dm, with optional path to JSON batch table data. Use "" for the path if there's no batch data to include.

### packcmpt ###
    ./packcmpt.py -o output_file input_file_1 [input file_2 ...]

`-o|--output`: Specify the path to the output cmpt file

License
-------
(c) 2016-2017 Geopipe, Inc. and licensed under the BSD 3-Clause license. See LICENSE.
