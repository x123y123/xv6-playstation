# xv6 Playstation
* Device: Macbook M1 Air
## ENV setting
* Install homebrew
```shell
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
### RISC-V tool chain
* Install riscv tool chain
```shell
$ brew tap riscv/riscv
$ brew install riscv-gnu-toolchain

# Testing whether the download is success
$ riscv64-unknown-elf-gcc --version
```
* Setting Environment Variables 
```shell
# Because I use zsh, so I configure the .zshrc, add followings in .zshrc:
export RISCV_HOME=/opt/riscv-gnu-toolchain
export PATH=${PATH}:${RISCV_HOME}/bin
```

### Qemu
* Install Qemu
```shell
$ brew install qemu
```
* Setting Environment Variables 
```shell
# Because I use zsh, so I configure the .zshrc, add followings in .zshrc:
export QEMU_HOME=/opt/qemu
export PATH=${PATH}:${QEMU_HOME}/bin
```
* Check qemu by version
```shell
$ qemu-system-riscv64 --version
```
