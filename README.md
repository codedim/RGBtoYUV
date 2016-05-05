# RGB to YUV converter

**rgb2yuv** converts RGB (24bpp Bitmap File) to YUV (NV12 pixelformat raw Frame) and vice versa.

**Note:** You can use `ffmpeg -i image.bmp -pix_fmt nv12 image.yuv` command to do the same things, 
but while you not need to play with raw data.

## Restriction 

The Width and Height Values of the Image must be multiple of Four!

## Build

**rgb2yuv** is a crossplatfofm utility and can be build with the following command:

`
  gcc -s -O2 -Wall rgb2yuv.c -o rgb2yuv
`

## Uses

#### To convert a Bitmap File to NV12 raw Frame:

`
  rgb2yuv image.bmp
`

You can upload your `image.yuv` file on [rawpixels.net](http://rawpixels.net/) to see the picture, 
for example.

####To convert a NV12 raw Frame to Bitmap File:

`
  rgb2yuv WxH frame.yuv
`

where:
* `W`  - frame width;
* `H`  - frame height.

**Note:** You have to know the Width and Height Values of the Frame before.
