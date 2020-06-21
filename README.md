# Hackintosh-EFI-huanan_B75
## 硬件配置
- CPU	Intel E3 1230 v2
- 主板	华南金牌B75
- 显卡	迪兰恒进RX460 4g
- 内存	16g
- 网卡	BCM94360CD	

## 安装简要
- ![主板bios设置](https://github.com/LeUKi/Hackintosh-EFI-huanan_B75/blob/master/B75-Bios-setting.md)
- 镜像用balenaEtcher刷进U盘
- 在macos环境下用disktuil指令挂载U盘的EFI分区（Windows用第三方工具）
- 替换U盘的EFI文件（驱动完善差不多了，需要最后自取）
- 插到主板USB2.0接口，关闭应该关闭的BIOS选项，U盘启动
- 如果正确替换了EFI就能进到安装界面了，剩下的就是常规流程
- 安装完系统后，同样使用disktuil指令挂载安装盘的EFI分区，把U盘的EFI文件替换进去（这里可能涉及两次的分区挂卸载，在没有Clover configurator软件的时候只能这样手动输入）

```bash
disktuil list
sudo disktuil mount diskXsX
sudo disktuil unmount diskXsX
```

    
