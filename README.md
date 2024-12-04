# B8261-genoa-edk2-helper

1. This is source code setup repository for MiTAC B8261 of Genoa/OpenSIL/EDK2.
2. Supported platform: B8261T85E24HR-2T (https://www.mitaccomputing.com/Barebones_TN85B8261_B8261T85E24HR-2T_EN~Spec)


## Clone Repositories

1. Execute init.sh to clone source codes and apply patches
2. The repositories and folder structure will be:
  - AGCL-R (Branch: genoa_poc)
  - amd_firmwares (Branch: genoa_poc)
  - AmdOpenSilPkg
    - opensil-uefi-interface (Branch: genoa_poc)
      - OpenSIL (Branch: genoa_poc)
  - edk2 (Branch: edk2-stable202205)
  - edk2-platforms (Tag: b8ffb76b471dae5e24badcd9e04033e8c9439ce3)
  - Patches
  - Platform (Branch: genoa_poc)


## Build and Deploy

1. Execute ./dbuild.sh b8261 --edk2args="-b DEBUG" to build debug rom
2. Deploy R8200000000N.FD to 32MB SPI flash of B8261


## Progress

- With these repositories, B8261 + Genoa can boot to EDK2 Shell successfully
- Debug messages are available through BMC SOL
- Only verify in Linux build environment


## Reference

- All openSIL related repositories are forked from https://github.com/openSIL; the projected plan is also aligned with AMD's roadmap of openSIL
- Aspeed Driver version is 1.13.05 from Aspeed website (BmcGopDxe)
