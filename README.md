# Flash-Blip for AuroraOS

Port of [Flash-Blip](https://github.com/plinkr/flash-blip) to [AuroraOS](http://auroraos.ru)

<div align="center">
  <img src="aurora_flash-blip_screenshot.png" alt="AuroraOS ScreenShot" width="240" style="display:inline-block; margin-right:8px; border-radius:8px;"/>
  <img src="aurora_flash-blip_screenshot2.png" alt="AuroraOS ScreenShot2" width="240" style="display:inline-block; margin-right:8px; border-radius:8px;"/>
  <img src="aurora_flash-blip_screenshot3.png" alt="AuroraOS ScreenShot3" width="240" style="display:inline-block; margin-right:8px; border-radius:8px;"/>
</div>

# Build
- download and install [AuroraSDK](https://developer.auroraos.ru/doc/software_development/sdk/downloads)
- list avaliable targets (use sfdk tool from SDK)
    ```
    ~/AuroraOS/bin/sfdk engine exec sb2-config -l
    ```
    its show something like
    ```
    AuroraOS-5.1.3.85-MB2-aarch64.default
    AuroraOS-5.1.3.85-MB2-aarch64
    AuroraOS-5.1.3.85-MB2-armv7hl.default
    AuroraOS-5.1.3.85-MB2-armv7hl
    AuroraOS-5.1.3.85-MB2-x86_64.default
    AuroraOS-5.1.3.85-MB2-x86_64
    ```
    where target names with `.default` suffixes - its snapshots. 
- Choose target "AuroraOS-5.1.3.85-MB2-aarch64" and build an RPM
    ```
    ~/AuroraOS/bin/sfdk -c "target=AuroraOS-5.1.3.85-MB2-aarch64" build-init
    ~/AuroraOS/bin/sfdk -c "target=AuroraOS-5.1.3.85-MB2-aarch64" prepare
    ~/AuroraOS/bin/sfdk -c "target=AuroraOS-5.1.3.85-MB2-aarch64" build
    ```
