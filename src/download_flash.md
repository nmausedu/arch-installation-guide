# Download/Flash

## Acquire an Arch Linux image file
The image file contains all you will need to perform the installation, so it is critical that when you download it, your download isn't interfered with.
To make sure of this, Arch provides `checksums` to make sure that the file you downloaded is the same file that you intended to download.

### Downloading the file

From <https://archlinux.org/download/> identify the closest mirror to your location.
From that mirror, download both the image file `archlinux-x86_64.iso` and the checksums `sha256sums.txt`

### Verifying the checksum

You will need different tools to verify the checksum, depending on your current operating system.

#### Windows
```
$ CertUtil -hashfile archlinux-x86_64.iso SHA256
```

#### MacOS
```
$ sha356sum archlinux-x86_64.iso
```

#### Linux
```
$ shasum -a 256 archlinux-x86_64.iso
```

## Flash the image file to a USB drive

Once you have the image file, you will need to flash it to a USB drive.
We recommend using balena etcher to accomplish this, which you can download from <https://www.balena.io/etcher>.

Your USB drive will be erased during the flashing process, so make sure any important information has been stored elsewhere first.

Once your drive is ready to be flashed, insert it into your computer.
Then, run balena etcher and select `archlinux-x86_64.iso` as your image, and your USB drive as the drive.
After that, click "Flash" to start the flash process.

If there are no errors, your drive will no longer be readable by your operating system.
This means that your drive is now bootable, and you can use it to install Arch Linux on any machine you'd like.

