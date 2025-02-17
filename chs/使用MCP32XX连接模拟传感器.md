

[开始页](../README.md) | [上一页](轴的连接.md) | [English](../eng/Connecting-analog-axes-to-MCP320x.md)

MCP32XX是一个系列的模拟数字转换器（ADCs）。有1通道、2通道、4通道和8通道等型号，名称中的最后一个数字代表能够连接的模拟通道数量。MCP32XX使用SPI接口工作。

![](../images/A1.6.jpg)
 
* SPI_SCK - 时钟信号，对所有SPI设备都一样（TLE5011, MLX90393, MCP32XX和所有的移位寄存器）；
* SPI_MISO - 主设备数据输入，从设备输出，对所有SPI设备都一样；
* SPI_MOSI - 主设备数据输出，从设备输入，对所有SPI设备都一样；
* MCP320x_CS - 片选信号，每个ADC单独连接。

其它型号的ADC使用同样的方式连接。不同型号的MCP32XX的引脚分配图如下：

![](../images/A1.6.1.jpg)

我们还从没看到过有已经安装在PCB板上的MCP32XX芯片，所以我们建议自己设计PCB板。

或者你可以使用转接板，比如MCP3201和MCP3202可以用这个：

![](../images/SO-8.jpg)

或者MCP3204和MCP3208可以用这个：

![](../images/SO-16.jpg)

这些ADC有不同的封装选择：DIP-8、DIP-16用于直插安装，SO-8、SO-16用于贴片安装。上面的转接板是为SO-8、SO-16封装的ADCs设计的。

[电位器](./电位器的连接.md)、[霍尔传感器](./霍尔传感器的连接.md)或者任何其它类型的模拟传感器，只要它们的输出信号范围在0-3.3V之间，就可以用作外部ADC的信号源。

当需要减少传感器的连线数量时（比如在摇杆中），或者是需要减少长导线的电磁干扰时（在这种情况下需要把ADC连接在离模拟信号源近的地方），可以使用ADC连接模拟传感器。

[轴的配置](轴的配置.md)部分会说明接下来在FreeJoy的配置程序中如何配置轴。

[开始页](../README.md) | [上一页](轴的连接.md) | [English](../eng/Connecting-analog-axes-to-MCP320x.md)
