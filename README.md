# MORepairPriority

《心灵终结 3.3.6》（Mental Omega 3.3.6）的客户端插件。

## 功能

- 维修单位（含 IFV 医生）自动优先修理血量百分比最低的友军
- 目标变化需要血量差超过阈值，避免来回切换

## 配置

```ini
[RepairPriority]
Enable=1
Interval=1        ; 扫描间隔（逻辑帧）
RadiusCells=6     ; 取不到武器射程时的回退半径
Hysteresis=3      ; 新目标至少低这么多百分比才换
Log=1
```
## 安装

1. 需要先安装 [Syringe](https://github.com/Ares-Developers/Syringe)（心灵终结自带）。
2. 把本目录下的文件放进游戏根目录（`gamemd.exe` 所在目录）。
3. 启动游戏即可。删除文件即卸载。

## 说明

- 纯客户端插件：不修改游戏模拟数据、不发送指令，联机时对方无需安装。
