# 更新日志

## [New]
    1.新增判定frame隐藏的接口
    2.新增判定目标点对单位可通行性，以及获取修正后的xy坐标的接口
    3.新增获取聊天框的接口
    4.解锁了加载阶段的字节码限制，现在不会出现触发器过多导致失效的问题了
    5.新增判定玩家单位/技能/物品/科技可用性的接口
    6.新增获取文本限制的接口
    7.新增设置物品碰撞类型的接口
    8.新增slk读取物编的接口
    9.修改技能命令支持所有继承自AAsp的技能
    10.新增任意单位获取仇恨目标事件
    11.jass追踪新增获取handle类型的功能
    12.新增任意单位被创建事件
    13.新增可设置凶手单位的杀死单位函数
    14.新增在任意时刻获取死亡单位的凶手单位的接口
    15.新增转换事件ID为整数(t)
    16.新增设置单位技能自定义物编字符串数据的接口
    17.新增设置特效动画播放速度的接口
    18.新增获取内存占用的接口
    19.崩溃报告中新增内存占用信息

## [Fix]
    1.修复部分地图加载器失效的bug
    2.修复设置绝对锚点时，锚点参数错误导致崩溃的bug
    3.修复冷却绘制工作不正常的bug
    4.修复设置投射物命中伤害t封装不正确的bug
    5.修复攻击出手事件导致原生法球失效的bug
    6.修复frame事件注册不正确的bug
    7.修复设置文本对齐方式对CTextFrame崩溃的bug
    8.修复进入0s的cd导致指示器被取消的bug
    9.修复MHFrame_SetText对TextButton等使用导致崩溃的bug
    10.修复判定frame隐藏t封装不正确的bug
    11.修复设置进度计时器进度1无效的bug
    12.修复设置技能自定义数据回收不正常的bug

## [Chg]
    1.修改dll的解压路径
    2.更改jass接口的内容，避免w2l优化脚本警告
    3.jass追踪去掉函数耗时统计
    4.修改MH的伤害事件的名称: 任意单位接受伤害->任意单位即将受伤
    5.修改判定普攻伤害的函数名称：是攻击伤害->是物理伤害
    6.对部分其他api的hook做了兼容
    7.修改MemHackLoader文件，请务必更新该文件
    8.设置单位技能自定义数据后自动更新信息栏

## [Old]
    1.更改设置文本限制的函数名: MHFrame_SetTextLength->MHFrame_SetTextLimit
    2.更改设置单位技能自定义物编数据的接口