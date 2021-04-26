# libsimpeleRF
c#
## simpleRF无线传感器网络调试串口通信 ##
#### 本实验主要是学习怎么配置CC2530RF功能。 ####
_本实验主要分为3大部分，第一部分为初始化与RF相关的信息_

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
