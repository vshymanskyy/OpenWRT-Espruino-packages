# OpenWRT-Espruino-packages
Espruino v1.94 package for OpenWRT

## Build from source

```bash
echo "src-git espruino git://github.com/vshymanskyy/OpenWRT-Espruino-packages.git" >> ./feeds.conf
./scripts/feeds update -a
./scripts/feeds install -p espruino -a
make menuconfig
```
Select ```Languages -> JavaScript -> espruino```
```
make -j9
```

## Build just Espruino
```
make package/espruino/compile V=s
```

## Rebuild Espruino
```
make package/espruino/{clean,compile,install} V=s
```
