# Cloud vendors

## Todos

- are there any FreeBSD-native cloud hosts? i.e. using bhyve
  (https://people.freebsd.org/~blackend/doc/handbook/virtualization-host-bhyve.html)


## Vultr
Says it's using KVM virtualisation, but from the looks of it inside a FreeBSD it
seems like it's Xen.

Using the default ISO image it's about ~2.5GB base install. I managed to
uploading a custom ISO from
https://download.freebsd.org/releases/amd64/amd64/ISO-IMAGES/13.1/ installing a
minimum install of ~500MB.
My experience was that it took a while to it to boot the custom ISO, it runs the
boot process pretty quickly but almost seems like it hangs but after 3-4 mins
you finally get to the bsdinstall start screen, so just be patient :)
