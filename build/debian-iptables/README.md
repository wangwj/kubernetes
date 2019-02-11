### debian-iptables

Serves as the base image for `harbor.ultra.com/k8s/kube-proxy-${ARCH}` and multiarch (not `amd64`) `harbor.ultra.com/k8s/flannel-${ARCH}` images.

This image is compiled for multiple architectures.

#### How to release

If you're editing the Dockerfile or some other thing, please bump the `TAG` in the Makefile.

```console
Build and  push images for all the architectures
$ make all-push
# ---> harbor.ultra.com/k8s/debian-iptables-amd64:TAG
# ---> harbor.ultra.com/k8s/debian-iptables-arm:TAG
# ---> harbor.ultra.com/k8s/debian-iptables-arm64:TAG
# ---> harbor.ultra.com/k8s/debian-iptables-ppc64le:TAG
# ---> harbor.ultra.com/k8s/debian-iptables-s390x:TAG
```

If you don't want to push the images, run `make build ARCH={target_arch}` or `make all-build` instead


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/build/debian-iptables/README.md?pixel)]()
