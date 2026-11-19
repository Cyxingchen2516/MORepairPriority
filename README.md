# MORepairPriority

《心灵终结 3.3.6》（Mental Omega 3.3.6）的客户端插件。

## 功能

维修单位（维修无人机、工程师 IFV、矿甲虫等）会自动把维修目标换成更值得修的那个：

- `Mode=lowest`：优先修**血量百分比最低**的友军（发 Attack，会停下瞄准）；
- `Mode=nearest`：优先修**最近**的残血友军（发 AttackMove，边移动边修，与原版 Ctrl+Shift 移动攻击一致）。

## 安装

1. 需要先安装 [Syringe](https://github.com/Ares-Developers/Syringe)（心灵终结自带）。
2. 把 `MORepairPriority.dll`、`MORepairPriority.dll.inj`、`MORepairPriority.ini` 放进游戏根目录。
3. 启动游戏即可。

## 配置

```ini
[RepairPriority]
Enable=1
Interval=1        ; 扫描间隔（逻辑帧）
RadiusCells=6     ; 取不到武器射程时的回退半径
Hysteresis=3      ; 新目标至少低这么多百分比才换（仅 Mode=lowest）
Mode=nearest      ; nearest = 最近残血 + 边移动边修；lowest = 最低血 + 停下修
EngineerTypes=    ; 额外工程师类型 ID
Log=1
```

## 说明

- 纯客户端插件：只读对象状态、发送标准事件，不修改模拟数据。
- 联机时对方无需安装。

## 兼容

- 心灵终结 3.3.6（gamemd + Syringe 0.7.3 + Ares 3.0p1）
