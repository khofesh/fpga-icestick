# Lattice iCEstick evaluation board

<img src="./images/20230502_120320_reduced.jpg" width="300" height="200" alt="theboard">

## setup

https://github.com/FPGAwars/apio/wiki/Quick-start

### 1. apio

create new python virtual environment and install apio there.

```shell
virtualenv ~/fpgaenv
source ~/fpgaenv/bin/activate
pip install -U apio
```

### 2. install all the available apio packages

```shell
(fpgaenv) [fahmad@ryzen fpga-icestick]$  which apio
~/fpgaenv/bin/apio
(fpgaenv) [fahmad@ryzen fpga-icestick]$  apio --version
```

### 3. enable ftdi

```shell
apio drivers --ftdi-enable
```

list

```shell
(fpgaenv) [fahmad@ryzen fpga-icestick]$ apio system --lsftdi
Number of FTDI devices found: 1
Checking device: 0
Manufacturer: FTDI, Description: Dual RS232-HS
```

### 4. examples

```shell
apio examples -l
apio examples -d icestick/leds
```

list supported boards and create `apio.ini`

```shell
apio boards --list
apio init --board icestick
```

verify

```shell
apio verify
```

simulate

```shell
sudo dnf install gtkwave
apio sim
```

build

```shell
apio build
```

# References

- https://www.youtube.com/playlist?list=PLEBQazB0HUyT1WmMONxRZn9NmQ_9CIKhb
- https://yosyshq.net/yosys/about.html
- https://wiki.archlinux.org/title/Python/Virtual_environment
- https://appcodelabs.com/getting-started-with-lattice-icestick-using-open-source-tools-on-macos-linux
