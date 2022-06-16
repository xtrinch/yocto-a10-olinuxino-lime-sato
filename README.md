# yocto-a10-olinuxino-lime

Use dunfell branches, kirkland has errors.

`source poky/oe-init-build-env build`
`bitbake-layers show-layers`
`bitbake -c menuconfig virtual/kernel`

Basic X11 terminal:
`bitbake core-image-x11`
Burn to sd `build/tmp/deploy/images/olinuxino-a10lime/core-image-x11-olinuxino-a10lime.sunxi-sdimg`

`bitbake core-image-sato`
Burn to sd `build/tmp/deploy/images/olinuxino-a10lime/core-image-sato-olinuxino-a10lime.sunxi-sdimg`
