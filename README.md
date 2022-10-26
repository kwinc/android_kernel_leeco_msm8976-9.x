# android_kernel_leeco_msm8976-9.x
---
How to

```
mkdir toolchain
cd toolchain
wget https://releases.linaro.org/components/toolchain/binaries/4.9-2017.01/aarch64-linux-gnu/gcc-linaro-4.9.4-2017.01-x86_64_aarch64-linux-gnu.tar.xz
tar -xf gcc-linaro-4.9.4-2017.01-x86_64_aarch64-linux-gnu.tar.xz
cd ..
export ARCH=arm64 CROSS_COMPILE=$PWD/toolchain/gcc-linaro-4.9.4-2017.01-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-

git clone https://github.com/kwinc/android_kernel_leeco_msm8976-9.x --depth 1 --single-branch
cd android_kernel_leeco_msm8976-9.x
mkdir out
make -j$(nproc --all) -C $PWD O=$PWD/out nethunter_c106_defconfig
make -j$(nproc --all)
```

