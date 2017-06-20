# OpenWRT-Espruino-packages
Espruino package for OpenWRT

Build from source:

```bash
echo "src-git espruino git://github.com/vshymanskyy/OpenWRT-Espruino-packages.git" >> ./feeds.conf
./scripts/feeds update -a
./scripts/feeds install -p espruino -a
make menuconfig
```
Select ```Languages -> JavaScript -> espruino```
```
make -j 9
```

To build just Espruino:
```
make package/espruino/compile V=s
```

For a rebuild:
```
make package/espruino/{clean,compile,install} V=s
```
