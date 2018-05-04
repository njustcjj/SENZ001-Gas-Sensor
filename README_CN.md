# SENZ001 模拟气体传感器###### 翻译> `英文`请参考 [`这里`](https://github.com/njustcjj/SENZ001-Gas-Sensor/blob/master/README.md).> `中文`请参考 [`这里`](https://github.com/njustcjj/SENZ001-Gas-Sensor/blob/master/README_CN.md).![](https://github.com/njustcjj/SENZ001-Gas-Sensor/blob/master/pic/SENZ001_front.jpg "SENZ001_Front") ![](https://github.com/njustcjj/SENZ001-Gas-Sensor/blob/master/pic/SENZ001_back.jpg "SENZ001_Back") ### 产品介绍> SENZ001是基于QM-N10探头，以Sn02材料作为敏感基体制作的广谱性气体传感器。> 该产品的最大特点是对各种可燃性气体(如氢气、液化石油气、烷烃类等气体)以及酒精、烟雾等有毒气体具有高度的敏感性。> > 用途：常与风扇、儿童玩具搭配，用于家庭和工厂气体污染、泄漏的检验、提醒、报警。### 产品参数#### 标准电路条件* 加热电压( VH )：5±0.2V ( AC or DC )* 回路电压( VC )：10V ( 最大 DC 24V)* 负载电阻( RL )：2KΩ(可自定)* 清洁空气中电压( V0 )：≤1.5V* 元件功耗：≤0.9W

#### 标准测试电路条件下气敏元件特性* 输入电压( VC )：5±0.1V 
* 电流：150 mA
* 加热电阻( R<sub>H</sub> )：31±3Ω
* 预热时间：≥48h
* 灵敏度：≥5
* 响应时间( tres )：≤10S* 恢复时间( trec )：≤30S
* 外形尺寸( L*W*H )：32x20x22mm### 使用教程#### 引脚定义> AO脚        -模拟信号输出> 
> DO脚        -TTL开关信号输出
> > GND脚   -电源地>> VCC脚   -电源正##### 用法及注意事项1. 元件开始通电工作时，没有接触丁烷气体，其电导率也急剧增加，约一分钟后达到稳定，这时方可正常使用，这段变化在设计电路时可采用延时处理解决。2. 加热电压的改变会直接影响元件的性能，所以在规定的电压范围内使用为佳。3. 元件在接触标定气体1000ppm丁烷后10秒钟以内负载电阻两端的电压可达到 ( Vdg-Va )差值的70% ( 即响应时间 )；脱离标定气体1000ppm丁烷30秒钟以内负载电阻两端的电压下降到 ( Vdg -Va )差值的70% ( 即恢复时间 )。4. 符号说明 * 检测气体中传感器电阻-Rdg * 检测气体中传感器电压-Vdg    Rdg与 Vdg的关系：Rdg=RL(VC/Vdg-1)5. 负载电阻可根据需要适当改动，以满足设计的要求。6. 使用条件：温度-15~40℃；相对湿度20～85%RH；大气压力80～106KPa。7. 环境温湿度的变化会给元件电阻带来小的影响，可进行湿度补偿，最简便的方法是采用热敏电阻补偿之。8. 避免腐蚀性气体及油污染，长期使用需防止灰尘堵塞防爆不锈钢网。#### 连线图以输出检测值为例：![](https://github.com/njustcjj/SENZ001-Gas-Sensor/blob/master/pic/SENZ001_connect.png "连线图") ### 示例代码    void setup()     {       Serial.begin(9600); // 9600 bps    }    void loop()     {      int val;      val=analogRead(0);      Serial.println(val ,DEC);// 连续打印val值      delay(100);    }### 购买[*SENZ001 模拟气体传感器*](https://www.ebay.com/).