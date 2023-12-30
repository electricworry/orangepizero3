# This makefile is just an accessory for fast turnaround of building and testing.
# To use, source poky/oe... as normal then run make here.
# Not intended for production use.

.PHONY: build write

build:
	bitbake core-image-base

clean:
	bitbake -c clean linux-mainline && bitbake -c cleansstate linux-mainline

# write:
# 	sudo umount /dev/sdb?
# 	sudo bmaptool copy ./tmp/deploy/images/orange-pi-zero3/core-image-base-orange-pi-zero3.rootfs.wic.gz /dev/sdb

console:
	sudo tio /dev/ttyUSB0
