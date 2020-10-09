# OnePlus5Pkg
EDK2 (or EDK II) UEFI for OnePlus 5

Based on (parts of):
* [Zhuowei's port for Pixel3XL](https://github.com/Pixel3Dev/edk2-pixel3)
* [fxsheep's port for XiaomiMi6](https://github.com/fxsheep/edk2-sagit)
* [samzanemesis's port for FxtecPro](https://github.com/samzanemesis/FxtecProPkg)

## Building

### Dependencies (Ubuntu 18.04)
```bash
sudo apt install -y build-essential uuid-dev iasl git nasm python3-distutils gcc-aarch64-linux-gnu
```

### Initial setup
```bash
mkdir -p ~/EDK2 && cd ~/EDK2
git clone https://github.com/JamiKettunen/OnePlus5Pkg.git
git clone https://github.com/tianocore/edk2.git --recursive
git clone https://github.com/tianocore/edk2-platforms.git
./OnePlus5Pkg/firstrun.sh
```
**NOTE:** All clones in same directory!

### Build everything
```bash
./OnePlus5Pkg/build.sh
```

### Boot EDK2 UEFI image
```bash
fastboot boot uefi.img.
```

## Credits
SimpleFbDxe screen driver is from imbushuo's [Lumia950XLPkg](https://github.com/WOA-Project/Lumia950XLPkg).
