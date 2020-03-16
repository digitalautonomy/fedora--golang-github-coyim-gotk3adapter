To fix: To build you need to manually clone and generate the tar.gz expected by the spec file.
Spec files uploaded to Fedora's repo auto download the source code. I would fix this later.

```
git clone https://github.com/coyim/gotk3adapter.git
mv gotk3adapter gotk3adapter-8ad62a930093c5c48a13619223885d6ac3418bb0
tar zcf gotk3adapter-8ad62a930093c5c48a13619223885d6ac3418bb0.tar.gz gotk3adapter-8ad62a930093c5c48a13619223885d6ac3418bb0/
rm -rf gotk3adapter-8ad62a930093c5c48a13619223885d6ac3418bb0
```

To build this package you would need to install the `golang-github-gotk3-devel` package.

Building the package:
```
fedpkg --release f31 local
```