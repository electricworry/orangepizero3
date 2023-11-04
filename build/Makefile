
.PHONY: build write

build:
	bitbake core-image-minimal

clean:
	bitbake -c clean u-boot

me:
	rm workspace/sources/u-boot; ln -s u-boot.me workspace/sources/u-boot

them:
	rm workspace/sources/u-boot; ln -s u-boot.them workspace/sources/u-boot

write:
	sudo umount /dev/sdb1 /dev/sdb2
	sudo bmaptool copy ./tmp/deploy/images/orange-pi-zero3/core-image-minimal-orange-pi-zero3.rootfs.wic.gz /dev/sdb

console:
	sudo tio /dev/ttyUSB0
