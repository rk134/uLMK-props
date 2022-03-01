# uLMK prop enabler

This Magisk Module adds userspace LMK props to vendor/build.prop. On some kernels/ROMs, the ROM can act differently
and in unwanted ways, and this could be due to the lack of uLMK props.

## How to install:

## !!--WARNING--!!
I am not responsible for any damage caused to your device.
DO not PM me either asking you for help. 
Bug reports are only to be accepted in this format:

- Bugreport [DATE GOES HERE] [TIME GOES HERE]
- ROM: [ROM NAME GOES HERE]
- Kernel: [KERNEL NAME GOES HERE]
- Bug: [BUG DESCRIPTION GOES HERE]
- Log: [LOG GOES HERE, WITHOUT THEM I WILL PROVIDE NO SUPPORT!]

## Stable release:
1. Dowload latest uLMK-props.zip from releases page
   https://github.com/rk134/uLMK-props/releases
2. Disable MagiskHide: MagiskManager -> Settings -> Magisk Hide
3. MagiskManager -> Modules + Downloads/uLMK-props.zip -> Reboot

## release branch:

```
git clone https://github.com/rk134/uLMK-props -b release
cd uLMK-props
git archive --output uLMK-props.zip HEAD
adb push uLMK-props.zip /sdcard/

```
Then, 
- Disable MagiskHide: MagiskManager -> Settings -> Magisk Hide
- MagiskManager -> Modules + uLMK-props.zip -> Reboot

## Troubleshooting

### What to do if your device doesn't boot

How to unbrick:
1. Reboot to TWRP recovery
2. adb shell rm -fr /data/adb/modules/uLMK-props
3. adb reboot recovery

### ADB doesn't work

This means that adbd in your firmware is build without
ALLOW_ADBD_ROOT. You can fix adb autostart either by
installing evdenis' [ADB Root](https://github.com/evdenis/adb_root) module or disabling this module.


## Support

- [Telegram](https://t.me/joinchat/GsJfBBaxozXvVkSJhm0IOQ)
- [XDA Thread](https://forum.xda-developers.com/apps/magisk/module-debugging-modules-adb-root-t4050041)

## Credits

README.md based off evdenis' enable_eng module.
