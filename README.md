# yocto-a10-olinuxino-lime

Yocto poky distribution sato image for A10 Olinuxino Lime development board. 
(Sato image contains an X11 environment with a file browser, terminal, media player, ...)

Use dunfell branches, kirkland has errors.

## Usage

Activate env:
`source poky/oe-init-build-env build`

Add layers:
`cd build`
`bitbake-layers add-layer ../meta-openembedded/meta-oe`
`bitbake-layers add-layer ../meta-sunxi`

Verify layers:
`bitbake-layers show-layers`

Menuconfig:
`bitbake -c menuconfig virtual/kernel`
`bitbake -c menuconfig busybox` # tooling

Basic X11 terminal image:
`bitbake core-image-x11`
Burn to sd `build/tmp/deploy/images/olinuxino-a10lime/core-image-x11-olinuxino-a10lime.sunxi-sdimg`

Basic desktop image:
`bitbake core-image-sato`
Burn to sd `build/tmp/deploy/images/olinuxino-a10lime/core-image-sato-olinuxino-a10lime.sunxi-sdimg`

Other commands:
`bitbake -e | grep SOME_VARIABLE`