# 实验十一 #
## simpleRF无线传感器网络调试串口通信 ##
#### 本实验主要是学习怎么配置CC2530RF功能。 ####
~~使用c#编译~~
* __本实验主要是学习怎么配置CC2530RF功能。本实验主要分为3大部分，第一部分为初始化与RF相关的信息；__
* _第二部分为发送数据和接收数据；最后为选择模块功能函数。_
*其中模块功能的选择是通过开发板上的按键来 选择的
*          
>           其中按键功能分配如下：
>>            1. SW1 --- 开始测试（进入功能选择菜单）
>>            2. SW2 --- 设置模块为接收功能（Light）
>>            3. SW3 --- 设置模块为发送功能（Switch）
>>            4. SW4 --- 发送模块发送命令按键
```static uint8 pRxData[APP_PAYLOAD_LENGTH];  //接收数据数组

static basicRfCfg_t basicRfConfig;         //RF初始化结构体

extern void halboardinit(void);            //硬件初始化函数
extern void ctrPCA9554FLASHLED(uint8 led); //IIC灯控制函数
extern void ctrPCA9554LED(uint8 led,uint8 operation);
extern uint8 halkeycmd(void);              //获取按键值函数
```
| 左对齐 | 右对齐 | 居中对齐 |
| :-| -: | :-: |
| appRecive | appSend | appSelectMode |
| 接受 | 发送 | 切换模式 |
      

1.      当发送模块按下SW4时，将发射一个控制命令，接收模块在接收到该命令后，将控制LDE1的亮或者灭。
2.      其中LED6为工作指示灯，当工作不正常时，LED5将为亮状态。
3.      在\include\文件和\source\文件中包含了和RF相关的一些宏和函数，用户使用这些宏和函数可以简化对CC2530的RF操作，提高代码的可读性，本实验中就使用了其中的一些宏和函数。
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
        
* 主页 [readme](https://github.com/chenwenshuo0308/libsimpeleRF/blob/main/README.md)
