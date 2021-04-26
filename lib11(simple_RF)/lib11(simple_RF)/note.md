# 实验十一 #
## simpleRF无线传感器网络调试串口通信 ##
#### 本实验主要是学习怎么配置CC2530RF功能。 ####
_本实验主要分为3大部分，第一部分为初始化与RF相关的信息_
_第二部分为发送数据和接收数据；最后为选择模块功能函数。_
         
         static void appRecive()           //灯应用处理函数    
           static void appSend();                  //开关应用处理函数
         static uint8 appSelectMode(void);         //应用功能选择函数
        
函数名称：appRecive
*
*  功能描述：接收模式应用函数，初始化RF一些参数，接收另一个模块发送的控制命令，然后控制相应的LED灯
           
*               当发送模块按下SW4时，将发射一个控制命令，接收模块在接收到该命令后，将控制LDE1的亮或者灭。
*
*               其中LED6为工作指示灯，当工作不正常时，LED5将为亮状态。
 函数名称：appSend

* 功能描述：发送模式应用函数，初始化发送模式RF，通过按下SW4向另一个模块发送控制命令。             
        
*主页 [readme](https://github.com/chenwenshuo0308/libsimpeleRF/blob/main/README.md)
