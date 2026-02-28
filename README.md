# Debian Packaging for CEF 131

This is Debian packaging repository for the [Chromium Embedded Framework
v131](https://bitbucket.org/chromiumembedded/cef).

Precompiled Debian, Ubuntu and Raspberry Pi OS packages can be found here:

* https://cccp-linux.github.io/packages

Due to GitHub file size limitations, the additional original tarballs are not
included in the pristine-tar branch, and have to be downloaded separately:

```shell
p=chromium-embedded-131
v=131.4.1+g437feba

for n in amd64:64 arm64:arm64 armhf:arm; do
    a=`echo $n | cut -d: -f1`
    b=`echo $n | cut -d: -f2`
    wget -cO ../${p}_${v}.orig-${a}.tar.bz2 \
        https://cef-builds.spotifycdn.com/cef_binary_${v}+chromium-131.0.6778.265_linux${b}_minimal.tar.bz2
done
```

Share and enjoy.

## Authors

* **Dimitry Ishenko** - dimitry (dot) ishenko (at) (gee) mail (dot) com

## License

This project is distributed under the GNU GPL license. See the
[LICENSE.md](LICENSE.md) file for details.
