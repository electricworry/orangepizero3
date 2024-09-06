# Making a BSP for OrangePi Zero3

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