### debian-hyperkube-base

Serves as the base image for `harbor.ultra.com/k8s/hyperkube-${ARCH}`
images.

This image is compiled for multiple architectures.

#### How to release

If you're editing the Dockerfile or some other thing, please bump the `TAG` in the Makefile.

```console
# Build and  push images for all the architectures
$ make all-push
# ---> harbor.ultra.com/k8s/debian-hyperkube-base-amd64:TAG
# ---> harbor.ultra.com/k8s/debian-hyperkube-base-arm:TAG
# ---> harbor.ultra.com/k8s/debian-hyperkube-base-arm64:TAG
# ---> harbor.ultra.com/k8so/debian-hyperkube-base-ppc64le:TAG
# ---> harbor.ultra.com/k8s/debian-hyperkube-base-s390x:TAG
```

If you don't want to push the images, run `make all-build` instead


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/build/debian-hyperkube-base/README.md?pixel)]()
