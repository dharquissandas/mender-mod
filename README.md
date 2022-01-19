### Mender 64 bit conversion (so far)
This is an attempt to modify the mender convert code to see if I can get 64bit images to convert successfully with mender-convert.

## Current Problem after modifying code
The final output is an image that does build and it does boot but gets stuck booting into busybox rather than the actual partition. After tinkering some more I found out that if I changed the the root attribute in cmdline.txt to the partition like so root=/dev/mmcblk0p2 then it did in fact boot correctly into the necessary partition. But doing this obviously negates the point of using mender in the first place.
## Authors

Mender was created by the team at [Northern.tech AS](https://northern.tech),
with many contributions from the community. Thanks
[everyone](https://github.com/mendersoftware/mender/graphs/contributors)!

[Mender](https://mender.io) is sponsored by [Northern.tech AS](https://northern.tech).
