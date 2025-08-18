Talos extensions must be done via upgrade image.

Eg.

```
talosctl upgrade --preserve --image factory.talos.dev/installer/613e1592b2da41ae5e265e8789429f22e121aab91cb4deb6bc3c0b6262961245:v1.10.6 --nodes=192.168.1.64
```

The above hash contains the image for iscsi-tools and util-linux-tools

It seems dowloading the ISO which supposedly contains these tools does not work and you need to upgrade manually after installation.