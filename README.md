[TOC]

## CentOS 版本

- CentOS-6.7-x86_64-bin-DVD1.iso

## 安装步骤

### 1.载入 CenOS 镜像

点击“编辑虚拟机设置”，选择硬件下的“CD/DVD(IDE)”，然后选择“使用 ISO 映像文件”将 CenOS镜像载入。载入完成后，点击“开启此虚拟机”。

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/002.%E8%BD%BD%E5%85%A5centos%E9%95%9C%E5%83%8F.png)


### 2. 开启主板虚拟化

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/001.VMware%20Workstation%20Intel%20VT-x%20%E5%A4%84%E4%BA%8E%E7%A6%81%E7%94%A8%E7%8A%B6%E6%80%81.png)

在开启虚拟机后，可能会提示“Intel VT-X 处于禁用状态”。这是因为主板没有开启虚拟化导致的。
需要进入 BIOS，开启 Virtualization Technology。开启方法如下：

- 进入 BIOS 后。开机时按 F2 或 F12 或 DEL 或 ESC 等键（各品牌电脑有所不同）。
- 进入 BIOS 后，找到 Configuration 选项，选择 Intel Virtual Technology 并回车，将光标移至 Enabled，然后再回车，最后按 F10 保存并退出。

**如果找不到Configuration选项，可以试试下面的方法**：

- 某些 HP（惠普）电脑进入 BIOS 后，需要选择 SystemConfiguration（系统配置）菜单，然后选择 Device Configuration（设备配置），找到 Virtualization Technology，设置为 Enabled。
- 某些联想 Thinkpad 电脑进入 BIOS 后，需要选择 Security 菜单，然后选择 Virtualization，设置为 Enabled。
- 某些 DELL（戴尔）电脑进入 BIOS 后，需要选择 Processor Settings 菜单，然后选择 VirtualizationTechnology，设置为 Enabled。

### 3. 选择安装模式

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/003.%E9%80%89%E6%8B%A9%E5%AE%89%E8%A3%85%E6%A8%A1%E5%BC%8F.png)

选择第一项：**Install or upgrade an existing system**  安装或升级现有的系统，其他四项为：

- Install system with basic video driver 安装带有基本视频驱动的系统
- Rescue installed system 进入系统修复模式
- Boot from local drive 退出安装从硬盘启动
- Memory test 内存检测

**提示：安装过程中按下 ctrl + alt 键可以切换鼠标焦点。**


### 4. 检查光驱完整

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/004.%E6%A3%80%E6%9F%A5%E5%85%89%E9%A9%B1%E5%AE%8C%E6%95%B4.png)

这一步是提示用户检查光驱完整，直接选择 Skip 即可（使用 Tab 键选择）。

### 5. 进入 CentOs 安装界面

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/005.%E8%BF%9B%E5%85%A5Centos%E5%AE%89%E8%A3%85%E7%95%8C%E9%9D%A2.png)

选择 Next 即可。

### 6. 选择安装过程中的语言

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/006.%E9%80%89%E6%8B%A9%E5%AE%89%E8%A3%85%E8%BF%87%E7%A8%8B%E4%B8%AD%E7%9A%84%E8%AF%AD%E8%A8%80.png)

请选择英语，English（English），点击 Next 继续。

### 7.选择键盘布局

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/007.%E9%80%89%E6%8B%A9%E9%94%AE%E7%9B%98%E5%B8%83%E5%B1%80.png)

选择 U.S English，点击 Next。

### 8.选择存储设备

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/008.%E9%80%89%E6%8B%A9%E5%AD%98%E5%82%A8%E8%AE%BE%E5%A4%87.png)

选择第一项：Basic Storage Devices 基本存储设备，点击 Next 继续。

### 9. 存储设备警告

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/009.%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%AD%A6%E5%91%8A.png)

选择 Yes,discard any data.


### 10.输入主机名

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/010.%E8%BE%93%E5%85%A5%E4%B8%BB%E6%9C%BA%E5%90%8D.png)

输入主机名后，点击 Next 继续。

### 11.选择时区

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/011.%E4%B8%8B%E6%8B%89%E9%80%89%E6%8B%A9%E5%9C%B0%E5%8C%BA.png)

- 时区选择 Asia/Shanghai 亚洲/上海。
- 可通过下拉菜单选择，也可以点击地图选择。
- **System clock uses UTC** 该项不要勾选。

### 12.设置 root 密码

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/012.%E8%AE%BE%E7%BD%AEroot%E5%AF%86%E7%A0%81.png)

设置 root 密码完成后，点击 Next 继续。

### 13.磁盘分区

#### 13.1 选择磁盘分区方式

![](https://github.com/MorphiNerd/LinuxNote_2/blob/master/img/013_1.%E9%80%89%E6%8B%A9%E7%A3%81%E7%9B%98%E5%88%86%E5%8C%BA%E6%96%B9%E5%BC%8F.png?raw=true)

选择最后一项 **Create Custom Layout** 自定义分区方式。其他四项为：

- Use All Space：删除当前磁盘内的所有分区，包括其他系统创建的分区。
- Replace Existing Linux System(s)：删除当前磁盘内的所有 Linux 分区，而不删除其他系统创建的分区，该项为默认选项。
- Shrink Current System：利用分区上存在的所有空闲空间，创建系统默认的分区布局。
- Use Free Space：使用未使用的分区空间。

点击 Next 继续。

#### 13.2 选择标准分区

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_2.%E9%80%89%E6%8B%A9%E6%A0%87%E5%87%86%E5%88%86%E5%8C%BA.png)

选中你的硬盘，点击 Create，在弹出的 Create Storage 对话框中，选择 **Standard Partition** 标准分区。

点击 Create 继续。

#### 13.3 创建 /boot 分区

首先创建 /boot分区， /boot 分区用于存放系统内核与引导程序。

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_3.%E5%88%9B%E5%BB%BAboot%E5%88%86%E5%8C%BA.png)

- Mount Point 中输入 **/boot**。
- File System Type 选择 **ext4**。
- Size(MB) 为 **200 MB**。
- Force to be a primary partiton 该项 Check 上。

完成后点击 OK 继续。

#### 13.4 创建 swap 分区

第二步创建 swap 分区，它的作用相当于 Windows 里的虚拟内存。重复 “13.2 选择标准分区” 的操作，进入到 Add Partition 对话窗口。
（注意：要选中 Free 在点击 Create 进行分区。）

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_4.%E5%88%9B%E5%BB%BAswap%E5%88%86%E5%8C%BA.png)

- File System Type 选择 **swap**。
- Size(MB) 这里配置为 1500 MB。在内存小于 8G 的情况下，swap 分区的大小一般为物理内存容量的 1.5 倍。当系统物理内存大于 8G 时，swap 分区配置为 8G - 16G  即可。我们的虚拟机内存为 1G 所以这里配置为 1500 MB 。
- Force to be a primary partiton 该项 Check 上。

完成后点击 OK 继续。

#### 13.5 创建根分区

第三步创建根分区，它用来存放系统文件和程序。还是重复 “13.2 选择标准分区” 的操作，进入到 Add Partition 对话窗口。

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_5.%E5%88%9B%E5%BB%BA%E6%A0%B9%E5%88%86%E5%8C%BA.png)

- Mount Point 中输入 **/**。
- File System Type 选择 **ext4**。
- 选择 Fill to maximum allowable size 。
- Force to be a primary partiton 该项 Check 上。

完成后点击 OK 继续。

#### 13.6 格式化警告

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_6.%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%AD%A6%E5%91%8A.png)

选择 **Format** 。

#### 13.7 写入分区表

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/013_7.%E5%86%99%E5%85%A5%E5%88%86%E5%8C%BA%E8%A1%A8.png)

选择 **Write changes to disk**。

### 14. 选择引导

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/014.%E9%80%89%E6%8B%A9%E5%BC%95%E5%AF%BC.png)

这步默认即可，直接 Next 继续。

### 15. 选择系统安装类型

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/015.%E9%80%89%E6%8B%A9%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85%E7%B1%BB%E5%9E%8B.png)

选择 **Minimal** 最小化安装，然后底部选择 **Customize now**。

### 16. 选择系统安装包

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/016_1.%E9%80%89%E6%8B%A9%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85%E5%8C%85.png)

- 选择 Base System ，在右侧分别选择：Base、Compatibility libraries、Debugging Tools。

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/016_2.%E9%80%89%E6%8B%A9%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85%E5%8C%85-2.png)

- 选择 Development ,在右侧选择：Development tools。

点击 Next 继续。

### 17. 系统安装

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/017.%E5%BC%80%E5%A7%8B%E5%AE%89%E8%A3%85.png)

系统开始进行安装。

### 18.安装完成后重启

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/018.%E9%87%8D%E5%90%AF.png)

系统已经安装完成，点击 Reboot 重启。在启动过程中按 ESC 键可以查看启动过程。


### 19.进入系统

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/019.%E8%BF%9B%E5%85%A5%E7%B3%BB%E7%BB%9F.png)

输入用户名和密码后即可进入系统。（注意：Linux 下输入密码什么都不会显示）

### 20.后续操作

![](https://raw.githubusercontent.com/MorphiNerd/LinuxNote_2/master/img/020.%E5%90%8E%E7%BB%AD%E6%93%8D%E4%BD%9C.png)

安装完成后，需要将 ISO 镜像文件取出。

- 首先关机。
- 然后选择编辑虚拟机 - CD/DVD(IDE) - 使用物理驱动器。


## 扩展阅读

- [老男孩linux培训](https://blog.51cto.com/oldboy)

 


