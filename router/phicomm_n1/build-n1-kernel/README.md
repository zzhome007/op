# Build kernel for Phicomm-N1

If you use Phicomm N1 to install OpenWrt, you must know ‘Flippy’. He provides many versions of openwrt firmware for N1 and shares his series of kernels. If you have heard of ‘Flippy’ for the first time, you can find it through a search engine, E.g: Flippy n1 OpenWrt

## Usage

You can install Flippy’s OpenWrt firmware and use it. If you want to define some plug-ins and make your own dedicated op firmware, you can use this script to generate a kernel package adapted to this github source code. You have two ways to get the kernel, one is to use the kernel file provided by Flippy to synthesize (boot-${flippy_version}.tar.gz, dtb-amlogic-${flippy_version}.tar.gz & modules-${flippy_version}.tar.gz), another way is to use the Flippy’s Openwrt firmware file provided by him to extract. The operation of these two methods is as follows:

The first method: 
```shell script

Example: ~/op/router/phicomm_n1/build-n1-kernel/
 ├── flippy
 │   ├── boot-5.4.63-flippy-43+o.tar.gz
 │   ├── dtb-amlogic-5.4.63-flippy-43+o.tar.gz
 │   └── modules-5.4.63-flippy-43+o.tar.gz
 └── make_use_kernel.sh

```

put boot-${flippy_version}.tar.gz, dtb-amlogic-${flippy_version}.tar.gz & modules-${flippy_version}.tar.gz the three files into the ${flippy_folder} folder, run the script:
```shell script
sudo ./make_use_kernel.sh
```
The generated files will be directly placed in the kernel directory of this github: ` ~/op/router/phicomm_n1/armbian/phicomm-n1/kernel/${build_save_folder} `

The second method: 
```shell script

Example: ~/op/router/phicomm_n1/build-n1-kernel/
 ├── flippy
 │   └── N1_Openwrt_R20.8.27_k5.4.63-flippy-43+o.img
 └── make_use_img.sh
 
```

Put the Flippy’s OpenWrt firmware file ${flippy_file} into the ${flippy_folder} folder, run the script:
```shell script
sudo ./make_use_img.sh
```
The generated file will be placed directly in the kernel directory of this github: ` ~/op/router/phicomm_n1/armbian/phicomm-n1/kernel/${build_save_folder} `

## Tips

Use this github's Phicomm N1 to compile the code, you can customize ` default IP, hostname, theme, add/remove software packages `, etc. to generate special firmware.