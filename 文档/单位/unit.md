# 创建建筑
## jass定义
    function MHUnit_CreateBuilding takes player p, integer uid, real x, real y, boolean auto_build, boolean can_assist returns unit

## 参数
    p: 建筑所属玩家
    uid: 建筑单位ID
    x: 创建位置X坐标
    y: 创建位置Y坐标
    auto_build: 创建的建筑自动建造 (就像不死族建筑)
    can_assist：创建的建筑能被多敲 (就像人族建筑)

## 返回值类型
    单位

## 备注
    无



# 添加技能
## jass定义
    function MHUnit_AddAbility takes unit u, integer aid, boolean check_duplicate returns boolean

## 参数
    u: 添加技能的单位
    aid: 添加的技能
    check_duplicate: 检查相同技能

## 返回值类型
    真值

## 备注
    check_duplicate为false时，可添加相同技能。cj的UnitAddAbility会检查相同技能



# 删除技能
## jass定义
    function MHUnit_RemoveAbility takes unit u, integer aid, boolean check_duplicate returns boolean

## 参数
    u: 删除技能的单位
    aid: 删除的技能
    check_duplicate: 检查相同技能

## 返回值类型
    真值

## 备注
    check_duplicate为false时，可删除所有相同技能。cj的UnitRemoveAbility不会检查相同技能



# 获取技能
## jass定义
    function MHUnit_GetAbility takes unit u, integer aid, boolean search_base returns ability

## 参数
    u: 单位
    aid: 技能ID
    search_base: 通过基础ID查找

## 返回值类型
    技能

## 备注
    无



# 获取技能数量
## jass定义
    function MHUnit_GetAbilityCount takes unit u returns integer

## 参数
    u: 单位

## 返回值类型
    整数

## 备注
    包括魔法效果



# 获取指定序号的技能
## jass定义
    function MHUnit_GetAbilityByIndex takes unit u, integer index returns integer

## 参数
    u: 单位
    index: 序号

## 返回值类型
    技能

## 备注
    包括魔法效果



# 获取单位数据
## jass定义
    function MHUnit_GetData takes unit u, integer flag returns real

## 参数
    u: 单位
    flag: 数据类型 | UNIT_DATA

## 返回值类型
    实数

## 备注
    flag取值:
        UNIT_DATA_MAX_LIFE          最大生命值
        UNIT_DATA_MAX_MANA          最大魔法值
        UNIT_DATA_LIFE_REGEN        生命恢复速度
        UNIT_DATA_MANA_REGEN        魔法恢复速度
        UNIT_DATA_DEF_VALUE         护甲值
        UNIT_DATA_DEF_TYPE          护甲类型
        UNIT_DATA_POSITION_Z        Z轴坐标
        UNIT_DATA_CUR_SIGHT         当前视野
        UNIT_DATA_IMPACT_Z          射弹碰撞偏移-Z
        UNIT_DATA_IMPACT_Z_SWIM     射弹碰撞偏移-Z (深水)
        UNIT_DATA_LAUNCH_X          射弹碰撞-X
        UNIT_DATA_LAUNCH_Y          射弹碰撞-Y
        UNIT_DATA_LAUNCH_Z          射弹碰撞-Z
        UNIT_DATA_LAUNCH_Z_SWIM     射弹碰撞-Z (深水)
        UNIT_DATA_MODEL_SCALE       模型缩放
        UNIT_DATA_Z_SCALE           Z轴缩放
        UNIT_DATA_HPBAR_HEIGHT      血条高度
        UNIT_DATA_TIME_SCALE        动画播放速度
        UNIT_DATA_COLLISION         碰撞大小



# 设置单位数据
## jass定义
    function MHUnit_SetData takes unit u, integer flag, real value returns nothing

## 参数
    u: 单位
    flag: 数据类型 | UNIT_DATA
    value: 数值

## 返回值类型
    无

## 备注
    flag取值同 [获取单位数据](#获取单位数据)