# expansion_of_virtual_disk

## VirtualBox仮想ディスクを増やす
1. 元の仮想ディスクをコピーする
```
C:\Program Files\Oracle\VirtualBox> VBoxManager.exe clonemedium disk <input_image> <outout_image>
```

2. コピーした仮想ディスクをリサイズする
```
C:\Program Files\Oracle\VirtualBox> VBoxManager.exe modifymedium disk <copy_image> --resize <size(MB)>
```
