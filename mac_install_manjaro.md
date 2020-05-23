下载 iso 
----

http://manjaro.org/

创建可启动USB
----

  * 使用 diskutil 工具，写入 manjaro 系统
  
    ```
    diskutil list
    diskutil unmountDisk /dev/diskN <— Change N with the number your USB flash disk mounted
    sudo dd if=manjaro-kde-x86_64.iso of=/dev/rdiskN bs=1m
    diskutil eject /dev/diskN
    ```
  * 分区
  
  * 创建可启动的u盘
  
    重启系统时，按住 `alt/option` 键，选择 EFI 磁盘启动进入 manjaro 的安装过程。
    
    然后创建 EFI 启动分区才能启动 Manjaro，选择之前创建的分区，点击编辑按钮，按照如下配置保存。
    
    ```
    Size: 200MB
    Content: Format
    File System: fat32
    Mount Point: /boot/efi
    Flags: boot, esp
    ```
    
    剩下的空间安装 Manjaro
    
    ```
    Partition Type: GPT
    File Syste: ext4
    Mount Point: /
    
    ```




> https://www.techonia.com/6156/install-manjaro-deepin-on-macbook-pro

