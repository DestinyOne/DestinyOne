# Mac Notes

- ## NTFS 3G Installation

Install NTFS-3G from Homebrew by opening a Terminal and entering the following command.

    brew install ntfs-3g

After installing NTFS-3G you can manually mount NTFS volumes in read-write mode by executing the following commands in Terminal. Replace `/dev/disk1s1` with the actual NTFS partition you want to mount. You can find the partition name using `diskutil list`.

    sudo mkdir /Volumes/NTFS
    sudo /usr/local/bin/ntfs-3g /dev/disk2s1 /Volumes/NTFS -olocal -oallow_other
