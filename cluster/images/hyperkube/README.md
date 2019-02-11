### hyperkube

`hyperkube` is an all-in-one binary for the Kubernetes server components
`hyperkube` is built for multiple architectures and _the image is pushed automatically on every release._

#### How to release by hand

```console
# First, build the binaries
$ build/run.sh make cross

# Build for linux/amd64 (default)
# export REGISTRY=$HOST/$ORG to switch from staging-harbor.ultra.com/k8s

$ make push VERSION={target_version} ARCH=amd64
# ---> staging-harbor.ultra.com/k8s/hyperkube-amd64:VERSION
# ---> staging-harbor.ultra.com/k8s/hyperkube:VERSION (image with backwards-compatible naming)

$ make push VERSION={target_version} ARCH=arm
# ---> staging-harbor.ultra.com/k8s/hyperkube-arm:VERSION

$ make push VERSION={target_version} ARCH=arm64
# ---> staging-harbor.ultra.com/k8s/hyperkube-arm64:VERSION

$ make push VERSION={target_version} ARCH=ppc64le
# ---> staging-harbor.ultra.com/k8s/hyperkube-ppc64le:VERSION

$ make push VERSION={target_version} ARCH=s390x
# ---> staging-harbor.ultra.com/k8s/hyperkube-s390x:VERSION
```

If you don't want to push the images, run `make` or `make build` instead


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/cluster/images/hyperkube/README.md?pixel)]()
