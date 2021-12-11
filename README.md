# Montowanie obrazu APFS w Linux

  link do SIFT image: https://www.sans.org/tools/sift-workstation/

#### Przygotowanie SIFT Workstation
```
  # sudo apt-get update
  # sudo apt-get install libattr1-dev

  # sudo apt-get install libicu-dev
```
#### Ściągnąć i zbudować apfs-fuse
```
  # git clone https://github.com/sgan81/apfs-fuse

  # cd apf-fuse
  # mkdir build
  # cd build
  # cmake ..
  #  make
```
#### Mounting the E01 Image

###### ewfmount <image name> <mount point>
```
  # ewfmount mac_image.E01 /mnt/ewf
```
#### Montowanie the raw image to a loopback device

###### To run mmls on the mounted EWF:
  ```
  # mmls /mnt/ewf/ewf1
  # losetup -r -o 314597376 /dev/loop0 /mnt/ewf/ewf1
```
###### To run mmls on a dd/raw image
  ```
  # mmls mac_image.dd
  # losetup -r -o 314597376 /dev/loop0 mac_image.dd
  ```
#### Mount up the APFS filesystem
  ```
  # mkdir /mnt/apfs
  # ./apfs-fuse /dev/loop0 /mnt/apfs
```
