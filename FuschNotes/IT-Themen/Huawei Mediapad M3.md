Dateien liegen vom letzten flashen mit LineageOS 20 auf der Synology:
Home>Huawei MediaPad M3 Files

https://xdaforums.com/t/rom-13-0-lineageos-20-huawei-mediapad-m3-8-4-beethoven-update-27-09-2025.4647531/#post-89237875

Vorbereitung auf Windows PC:
ADB Treiber installieren (platform-tools)
Optional in die Umgebungsvariablen hinzufügen (https://www.xda-developers.com/install-adb-windows-macos-linux/)

Huawei Pad anschließen am PC
Im Geräte-Manager den Treiber installieren, falls notwendig. (https://www.driveridentifier.com/scan/generic-adb-interface-driver/driver-detail/F82E9218A8E6401B8EC23847BC0BC2B6/4632342/2e086f497bcbd98e6cdca490dd807ccc/822225827/USB-VID_18D1%26PID_D00D)

Huawei MediaPad in Fastboot booten über Volume Down + On/Off
fastboot flash recovery recovery.img

In Recovery booten über Volume Up + On/Off
adb sideload lineageos.zip

Dauert kurz ein paar Minuten
Reboot ins System