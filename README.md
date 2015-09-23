# OpenWRT-Espruino-packages
Espruino package for OpenWRT

Build from source:

```bash
echo "src-git node git://github.com/vshymanskyy/OpenWRT-Espruino-packages.git" >> ./feeds.conf
scripts/feeds/update -a
scripts/feeds/install -p espruino -a
make menuconfig
make -j 9
```
