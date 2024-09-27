# 安装配置wsl2的Ubuntu  
## 前言  
对于我这个连**Linux**和**wsl**都没听说过的超级大萌新，在艰难（粗浅）的学习了git和markdown的使用之后，带着一脸焦糖色的死气，抱着一碗方便面，在凌晨一点的宿舍开启了这段艰辛的历程  
左看右看，上看下看，发现招新题目这没有给出操作教程（怒），于是我毅然决然点开kimi，在文本框里输入  
`安装wsl,使用wls2,在 Windows 环境下虚拟出一个带有完整 Linux 内核的开发环境`  
kimi刷刷刷的出现了教程，豪德，虽然什么都看不懂，但是我还是开始了！！！  
* 安装wsl 
* 安装Linux  
* 更新linux最新版  


## 这是一段艰辛的历程  
### 安装wsl  
这里有[wsl指令的含义](https://learn.microsoft.com/zh-cn/windows/wsl/basic-commands)，妈妈再也不用担心我看不懂指令啦
1. 启用虚拟机平台
 >打开“控制面板” > “程序” > “启用或关闭Windows功能”。
 找到“虚拟机平台”，勾选它。
 点击“确定”，系统可能会要求您重启  

<img src="/1.png" width="50%">   

2. 启用wsl功能  
>打开 PowerShell 作为管理员。
运行以下命令来启用 WSL 功能：  

``` 
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart  
   ```  
<img src="/2.png" width="80%">

3. 设置 WSL 2 为默认版本
  > 打开 PowerShell 或 CMD 作为管理员。
   运行以下命令来设置 WSL 2 为默认版本：  

   `  wsl --set-default-version 2`  
![图片](/3.png)  

### 安装Linux  
1. 下载并安装 Linux 内核更新包
> 访问 WSL2 Linux 内核更新包的[官方下载页面](https://aka.ms/wsl2kernel)。  
下载与您的系统架构匹配的更新包（x64 ）。
安装下载的更新包。  

![图片](/4.png)  

2. 从 Microsoft Store 安装 Linux 发行版
  > 打开 Microsoft Store 应用，搜索linux，下载ubantu    

![图片](/5.png)  

3. 配置发行版本  
>首次启动时，将进行安装和配置过程，包括创建用户账户和密码  

**however，就在我跟着kimi教程走到这一步的时候，出现了错误**   
![图片](/6.png)
于是我把错误截图发送给kimi  
<img src="/7.png" width="60%">  
<img src="/8.png" width="60%"> 
我坚信不疑的跟着他的教程走，于是搞了一个多小时没有搞好  
我突发奇想，根据错误类型搜索对应的  [0x800701bc解决方案](https://zhuanlan.zhihu.com/p/599286889)
![picture](/9.png)    
我按着指令输入  
![picture](/11.png)
豪德，当我重启启动ubantu的时候，马上就安装好了，好了现在我知道下一步该干什么了  
* **把kimi掐死**  

### 更新Linux发行版  
掐死kimi之后（bushi）,我看着屏幕右下角的2:22，觉得我是个二货。  
然后我就继续操作  
1. 更新软件包列表

>先后输入指令  

`sudo apt update`    
`sudo apt upgrade `   
<img src="/12.png" width="50%">  
<img src="/13.png" width="50%">  
### 睡觉  
1. 托拖鞋  
2. 盖被子  
3. 闭上双眼  
<img src="/sleep.jpg" width="20%">

**豪德，完结撒花**  

  

## 个人感想  
虽然我是一个**随和**的人，但是：
![picture](/10.png)  
我<u>急眼</u>了 (划重点) 
在搞这个东西的过程中吧，我还是认识到了人工智能的力量，也在摸索之中找到了不少可以解决问题的途径，比如说哔哩哔哩，cdsn博客，知乎等，这让我收获颇丰  
但是还是要找寻多方面的资料，注意辨别
也让我认识到我这个小菜鸡在这个领域的弱小   

