# libsimpeleRF
c#
## simpleRF无线传感器网络调试串口通信 ##
#### 本实验主要是学习怎么配置CC2530RF功能。 ####
![吉林大学](https://github.com/chenwenshuo0308/libsimpeleRF/blob/main/%E5%90%89%E5%A4%A7.jpg)
[吉林大学杏花节]: https://news.jlu.edu.cn/__local/4/20/8C/42703A18EB7906D84EA69008ED1_C0A0F830_62528.jpg

_第二部分为发送数据和接收数据；最后为选择模块功能函数。_
*其中模块功能的选择是通过开发板上的按键来 选择的
*          
>           其中按键功能分配如下：
>>             SW1 --- 开始测试（进入功能选择菜单）
>>             SW2 --- 设置模块为接收功能（Light）
>>             SW3 --- 设置模块为发送功能（Switch）
>>             SW4 --- 发送模块发送命令按键
         
         static void appRecive()           //灯应用处理函数    

         static void appSend();                  //开关应用处理函数
         static uint8 appSelectMode(void);         //应用功能选择函数
 
      
*
*           当发送模块按下SW4时，将发射一个控制命令，接收模块在接收到该命令后，将控制LDE1的亮或者灭。
*
*           其中LED6为工作指示灯，当工作不正常时，LED5将为亮状态。
* 笔记 [note](https://github.com/chenwenshuo0308/libsimpeleRF/blob/main/lib11(simple_RF)/lib11(simple_RF)/note.md)
