环境：

1. 已解BL锁
2. win 电脑
3. 手机已安装magisk apk
4. FastBoot 工具
5. payload_dumper-win64 工具(可选)

## 步骤

1. 下载系统完整包，小米手机，系统更新那里，下拉出现【下载完整包】,点击下载，暂停，然后去下载管理那里重新开始。
2. 传统A-Only机型：在卡刷包第一层目录中就可以找到boot.img这个文件
3. VAB分区机型
    1. 解压出压缩包中的payload.bin文件
    2. 放到[[payload_dumper-win64](https://wwp.lanzouf.com/i5icDswxbih)](https://wwp.lanzouf.com/i5icDswxbih) payload_input的进行解压，在payload_output找到解压的boot.img文件
4. 打开Magisk app  安装 – 选择并修补一个文件 – 弹窗文件管理窗口（找到刚刚提取的**boot.img**
）- 开始，Magisk会生产一个magisk开头的img文件。
5. 手机连接到电脑，把**boot.img**和（**magisk_patched-2X000_xxxxx.img**）两个文件复制到电脑FastBoot根目录
6. 进入FastBoot文件，打开bat文件（**打开CMD命令行.bat**）把手机重启到Fastboot模式（**重启+音量-键**）然后输入下面的命令：fastboot flash boot +面具文件
7. 重启手机，查看Magisk是否刷入成功