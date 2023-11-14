
.PHONY: build write

build:
	bitbake core-image-x11

clean:
	bitbake -c clean linux-mainline && bitbake -c cleansstate linux-mainline

me:
	# rm workspace/sources/u-boot; ln -s u-boot.me workspace/sources/u-boot
	rm workspace/sources/linux-mainline; ln -s linux-mainline.me workspace/sources/linux-mainline

them:
	# rm workspace/sources/u-boot; ln -s u-boot.them workspace/sources/u-boot
	rm workspace/sources/linux-mainline; ln -s linux-mainline.them workspace/sources/linux-mainline

write:
	sudo umount /dev/sdb1 /dev/sdb2
	sudo bmaptool copy ./tmp/deploy/images/orange-pi-zero3/core-image-x11-orange-pi-zero3.rootfs.wic.gz /dev/sdb

console:
	sudo tio /dev/ttyUSB0
