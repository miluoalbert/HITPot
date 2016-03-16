#模块化无线电平台
#HITPot
#模块设计规范
==============

##简介
***
HITPot平台是一个模块化的无线电平台，其核心思想是每个硬件模块实现简单的功能，各个模块遵循统一的机械、电气以及软件规范，使得各个模块之间可以随意组合以实现用户期望的信号处理功能。
一个典型的Radio HITPot系统由一块底板，一块电源功能板和若干其他功能板组成，底板为各个功能板提供电气连接，各个功能板以层叠或平铺的形式固定在底板上，各个模块之间通过总线和同轴线进行连接。


##机械特性
***
###1.**外形尺寸**
HITPot可由标准板与非标准板组成，其中标准PCB板的外形与接插件的机械及电气定义均符合本规范中的相关定义；非标准PCB板则仅需要符合电气接口定义规范即可，对PCB板外形没有约束。除非有特别需求，否则应尽量使用标准PCB板。

***
	标准单元
- 单元PCB规格：50mm x 50mm 负公差1mm
- 二单元规格：100mm x 50mm 负公差1mm
- 四单元规格：100mm x 100mm 负公差1mm

螺柱固定孔是否金属化参考电气特性章节

***

###2.**连接器位置及尺寸**
连接器位于PCB板的一侧，可以采用多种规格的连接器，由于不同规格的连接器不能互相连接，因此当具有不同规格连接器的模块相互连接时，需要引入转接功能板。为了提高模块的兼容性，本规范推荐在没有特殊需要的情况下采用2.54mm间距的连接器进行连接。

![50x50mm标准外形单元板外形及接插件尺寸](https://raw.githubusercontent.com/miluoalbert/HITPot/Documents/Structure.png)
50x50mm标准外形单元板外形及接插件尺寸

![](https://raw.githubusercontent.com/miluoalbert/HITPot/Documents/Structure2.png)
![](https://raw.githubusercontent.com/miluoalbert/HITPot/Documents/Structure3.png)

***

##电气特性


|:-------:|:-------:|
| GND     | GND     |
| GND     | GND     |
| +5V     | +5V     |
| +5V     | +5V     |
| CAN_H   | CAN_L   |
| I2C_SCL | I2C_SDA |
| GPIO0   | GPIO1   |
| GPIO2   | GPIO3   |
| +12V    | +12V    |
| -12V    | -12V    |
| UART_Rx | UART_Tx |
| CAN_H   | CAN_L   |
| CAN_H   | CAN_L   |
| GPIO4   | GPIO5   |
| REVERSE | REVERSE |
| REVERSE | REVERSE |
| REVERSE | REVERSE |
| REVERSE | REVERSE |

***

##软件规范