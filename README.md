# Hackintosh-EFI-huanan_B75
已更新支援macOS12.0.1，其他版本请自行测试

安装前务必修改三码，安装完成后删除-v取消跑码

## 已知的反馈
- 兼容CPU E3 1230 v3
- 兼容主板 MSI B85-G43
- 可支援MacOS Monterey
- rx460 DP输出可能黑屏 (本人无问题)

## 硬件配置
- CPU	Intel E3 1230 v2
- 主板	华南金牌B75
- 显卡	迪兰恒进RX460 4g
- 内存	16g
- 网卡	BCM94360CD

## 安装简要
- [主板bios设置](https://github.com/LeUKi/Hackintosh-EFI-huanan_B75/blob/master/B75-Bios-setting.md)
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

## 更新
- 2.1 更新OpenCore7.5 支援 macOS 12.0.1 Monterey 正式版 21A559
- 2.0 转OpenCore 支援 macOS 11.0.1 Big Sur Developer beta11 20B5012d
- 1.3 修复config中内存信息残留导致的开机报错
- 1.2 更新clover5119;更新驱动;添加-v参数以支持新安装
- 1.1 支援 macOS 10.15.4 19E287
- 1.0 支援 macOS 10.15.3 19E266
