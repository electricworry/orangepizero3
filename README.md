# Making a BSP for OrangePi Zero3

This branch uses mainline linux.

```
bitbake core-image-minimal
```

## Crops

```
WORKDIR=$(echo $PWD | sed "s@/home/$USER@/home/pokyuser@")
docker run --rm -it -v $HOME/bitbake-downloads:/home/pokyuser/bitbake-downloads -v $HOME/bitbake-sstate-cache:/home/pokyuser/bitbake-sstate-cache -v $PWD:$WORKDIR crops/poky:ubuntu-22.04 --workdir=$WORKDIR
```

## Offline build

```
BB_NO_NETWORK = "1"
```

## Mainline doesn't work

Stuck at "Starting kernel ..."

However, changing kernel in layers/meta-sunxi/recipes-kernel/linux/linux-mainline-dev.bb to:

SRC_URI = "git://github.com/orangepi-xunlong/linux-orangepi;branch=orange-pi-6.1-sun50iw9;protocol=https \
	   file://defconfig \
"

And using defconfig-vendor in place of
layers/meta-sunxi/recipes-kernel/linux/linux-mainline-dev/aarch64/defconfig
works.

OpiZ2 6.6 works and instantly spits out to console.
OpiZ2 6.11 is the same.

Compare the "working" vendor fork to linux-stable 6.1.31 to find patches to resolve.

How to get over the lack of kernel output?
