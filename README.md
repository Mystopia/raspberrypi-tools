# raspberrypi-tools

## Getting Started

### Prepare your Raspberry Pi disk with Raspbian

 1. Download Raspbian
 1. Write the image to disk. There are plenty of ways to do this. Here is one of them:
  ```shell
  dd bs=1m if=2016-05-27-raspbian-jessie-lite.img | pv | sudo dd of=/dev/disk2 # if you have pv
  sudo dd bs=1m if=2016-05-27-raspbian-jessie-lite.img of=/dev/disk2 # if you do not
  ```

### Bootstrap your Raspberry Pi

Login to your Raspberry Pi to bootstrap and provision it.

  1. Bootstrap and provision using the `bootstrap` tool
   ```shell
   # Adafruit-Occidentalis takes care of a lot here, then we do a little bit more.
   # Inspect if you are paranoid.
   curl -SLs https://raw.githubusercontent.com/Mystopia/raspberrypi-tools/master/bin/bootstrap | less
   # Install when you are ready.
   curl -SLs https://raw.githubusercontent.com/Mystopia/raspberrypi-tools/master/bin/bootstrap | sudo bash
   ```
  1. Setup a hostname and WiFi by editing `/boot/occidentalis.txt`
