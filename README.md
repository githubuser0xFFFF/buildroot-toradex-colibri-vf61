# External buildroot packages for Toradex Colibri VF61
Unfortunately Toradex only supports [Open Embedded](http://developer.toradex.com/software-resources/arm-family/linux/board-support-package/openembedded-%28core%29) for building a Linux root filesystem for [Colibri VF61 board](https://www.toradex.com/de/computer-on-modules/colibri-arm-family/freescale-vybrid-VF6xx). For systems that require a great number of components or that require more advanced functionality, such as managing a package repository and supporting multiple hardware platforms at once for example, Open Embedded is the right choice and a powerful tool. But if you only want to build a filesystem image with only a few components, for a deeply embedded device (i.e. a CANopen motion controller, a temperature controller, a simple I/O node) [Buildroot](http://buildroot.uclibc.org/) remains much more appropriate. Buildroot is so much easier to use than Open Embedded. Therefore, it is really a disadvantage that Toradex only supports Open Embedded.

With the help of this repository you can use Buildroot to build a complete root filesystem for the Toradex Colibri VF61 board. Simply clone Buildroot and this repository to your local PC. Then cd into the Buildroot folder an type the following:

```
make BR2_EXTERNAL=/path-to-buildroot-toradex-colibri-vf61 vf61_min_defconfig
make
````
