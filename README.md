# Espruino for OpenWRT

This is **Espruino v1.94** package for **OpenWRT**.

 Espruino is an extremely compact JavaScript interpreter. Originally
 designed for microcontrollers, it runs on OpenWRT while using a very small
 amount of RAM.

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
