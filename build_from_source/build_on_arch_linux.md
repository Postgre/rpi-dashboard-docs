# Build on Arch Linux

1. Install git and rrdtool
```
sudo pacman -S git rrdtool python2 base-devel
```
2. Link python to python2
```
sudo ln /usr/bin/python2 /usr/bin/python
```
3. Install wiringPi
```
git clone git://git.drogon.net/wiringPi
(cd wiringPi && ./build)
```
4. Clone dudac repository
```
git clone https://github.com/monkey/dudac.git
```
5. Set up monkey and duda development environment in ~/.dudac:
```
dudac/dudac -s
```
If you want HTTPS instead of HTTP access, use:
```
dudac/dudac -sS
```
6. Clone duda-raspberry repository
```
git clone https://github.com/matematik7/rpi-dashboard.git
```
7. Checkout release version
```
(cd rpi-dashboard && git checkout tags/v0.2.0)
```
8. Build rpi-dashboard
```
dudac/dudac -w rpi-dashboard/src
```
If you want HTTPS instead of HTTP access, use:
```
dudac/dudac -Sw rpi-dashboard/src
```
