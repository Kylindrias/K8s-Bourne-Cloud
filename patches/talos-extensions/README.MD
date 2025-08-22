Talos extensions must be done via upgrade image.

Eg.

Linux-Utils
ISCSI Tools:

```
talosctl upgrade --preserve --image factory.talos.dev/installer/613e1592b2da41ae5e265e8789429f22e121aab91cb4deb6bc3c0b6262961245:v1.10.6 --nodes=10.105.62
```

Linux-Utils
ISCSI Tools
Xen Guest Tools:

```
talosctl upgrade --preserve --image factory.talos.dev/metal-installer-secureboot/58eedd04d458e2c900727f5a3af74a3ef6453b9902b23decb590c0007388187a:v1.10.6 --nodes=10.105.20.60
```

The above hash contains the image for iscsi-tools and util-linux-tools. These are required for Longhorn. The version number can be changed and the schematic ID will remain static for future use if you wish to upgrade to a later version.

It seems dowloading the ISO which supposedly contains these tools does not work and you need to upgrade manually after installation.

References:

https://longhorn.io/docs/1.9.1/deploy/install/install-with-flux/

https://www.talos.dev/v1.10/talos-guides/install/boot-assets/