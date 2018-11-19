---
layout: default
title: 伪代码描述洗衣机控制程序设计
---
# 伪代码描述洗衣机控制程序设计
## 聂硕琳 18342078
---

### 运用Top-down设计方法和Pseudocode 描述洗衣机控制程序。假设洗衣机可执行的基本操作如下：
_water_in_switch(open_close) // open 打开上水开关，close关闭_

_water_out_switch(open_close) // open 打开排水开关，close关闭_

_get_water_volume() //返回洗衣机内部水的高度_

_motor_run(direction) // 电机转动。left左转，right右转，stop停_

_time_counter() // 返回当前时间计数，以秒为单位_

_halt(returncode) //停机，success 成功 failure 失败_

1. 请使用伪代码分解“正常洗衣”程序的大步骤。包括注水、浸泡等；
> 1. 注水；
> 2. 检测水位达到某一高度后停止注水；
> 3. 电机开始转动，同时开始计时；
> 4. 返回时间计数，到时后停止转动； 
> 5. 打开排水开关； 
> 6. 停机。

2. 进一步用基本操作、控制语句（IF、FOR、WHILE等）、变量与表达式，写出每个步骤的伪代码；

```
SET time_limit, water_level_limit;
water_in_switch(open);
water_out_switch(close);
water_in_switch(open);
IF(water_level > water_level_limit){
    water_in_switch(close);
}
WHILE(time_counter() <= time_limit){
    motor_run(left);
    motor_run(tight);
}
motor_run(stop);
water_out_switch(open);
IF(water_level = 0){
    water_out_switch(close);
}
halt(success);

```

3. 根据你的实践，请分析“正常洗衣”与“快速洗衣”在用户目标和程序上的异同。
你认为是否存在改进（创新）空间，简单说明你的改进意见？
> 相同：目的相同、步骤相同；
> 
> 不同：程序的条件参量不同；