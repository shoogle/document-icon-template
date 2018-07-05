document-icon-template
======================

A "folded page" vector image template for creating document icons.

![Blank document icon][blank document icon]

[blank document icon]: standalone/document-icon-blank.svg "Blank document icon"

## Instructions

### Inkscape

[Inkscape]: https://inkscape.org/

[Inkscape] is a popular vector graphics editor which is free and open source.

If using Inkscape, open the [master template file] and edit the content layer.

### Other SVG editors

The layers feature may not work as intended in editors other than Inkscape,
so you may need to import the background and foreground layers as a separate
SVGs. These are available in the [standalone directory].

### Use as a library

[library example SVG]: standalone/document-icon-library-example.svg

It is possible for an SVG to reference external image files, including other
SVGs, using the following syntax:

```svg
  <image x="10" y="10" width="80" height="80" xlink:href="/path/to/image" />
```

This allows you to use an image resource in multiple SVGs without having to
store a separate copy of the image in each SVG. This saves disk space and
ensures that the SVGs are always up-to-date with any changes made to the
resource, without you having to manually re-import it into each one. The
[library example SVG] shows how you can do this with the background and
foreground standalone SVGs.

The downside of linked resources is that the SVG could become separated from
the resource and no longer render properly, and some SVG viewers can't handle
linked resources even when available. For these reasons, SVGs intended for
distribution should always use embedded resources rather than linked resources.
Linking is only suitable in master SVGs that are used to generate other
SVGs or raster images.

## Details

### Master SVG

[master template file]: document-icon-template-master.svg

The [master template file] is an Inkscape SVG with 3 layers:

1. Page and background shadow (background layer)
    - This is the blank page and border shadow.
    - You can change the shape or colour of the page by editing this layer.
2. Content layer
    - Normally this is the only layer you would edit.
    - Add your application logo or other design to this layer.
3. Curl and foreground shadows (foreground layer)
    - This is the curl or fold of the page, and associated shadows.
    - You can change the colour of the back of the page by editing this layer.

The master file contains special mark-up specific to the Inkscape editor. Other
programs may not be able to make full use of the information in this file.

### Standalone SVGs

[standalone directory]: standalone/

The files in the [standalone directory] are plain SVGs. You can use these files
with any SVG program to make new images of your own.

The standalone files are generated from the [master template file], so you need
to work on the master file if you want to make changes to the template itself.

## License

[CC0]: https://creativecommons.org/publicdomain/zero/1.0/

The Document Icon Template is released under the [Creative Commons Public
Domain Dedication (CC0 1.0 Universal)][CC0]. See [LICENSE.txt](LICENSE.txt)
for details.
