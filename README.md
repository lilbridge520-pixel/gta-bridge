# 霓虹城狂飙 Neon City Rush

一款赛博朋克风格开放城市赛车游戏（Windows x64，Godot 引擎）。

## 当前状态

`v0.1.0` — 可玩序章里程碑构建（2026-11-04，北京时间）。

- 引擎：Godot 4.7.2（Forward+ 渲染 / Jolt 物理）
- 可玩内容：序章「归城」完整可通关（步行、驾车、抢车追逐，约 12 分钟）
- 主线规划共 6 章：序章 → 第一章「旧路」→ 第二章「天穹」→ 第三章「重逢」→ 第四章「断桥」→ 终章「霓虹之巅」，目前仅序章已实现
- 开放区域：序章核内区域；其他城区尚在建设中（关区外灰平面属预期表现）

## 下载

游戏本体在 **Releases** 页面：

👉 https://github.com/lilbridge520-pixel/gta-bridge/releases/latest

因为 GitHub 单文件上传限制，游戏资源包 `NeonCityRush.pck` 被切成了 21 段（part001 ~ part021），下载后需要先合并：

**Windows（在下载目录执行 cmd）：**

```bat
copy /B NeonCityRush.pck.part001+NeonCityRush.pck.part002+NeonCityRush.pck.part003+NeonCityRush.pck.part004+NeonCityRush.pck.part005+NeonCityRush.pck.part006+NeonCityRush.pck.part007+NeonCityRush.pck.part008+NeonCityRush.pck.part009+NeonCityRush.pck.part010+NeonCityRush.pck.part011+NeonCityRush.pck.part012+NeonCityRush.pck.part013+NeonCityRush.pck.part014+NeonCityRush.pck.part015+NeonCityRush.pck.part016+NeonCityRush.pck.part017+NeonCityRush.pck.part018+NeonCityRush.pck.part019+NeonCityRush.pck.part020+NeonCityRush.pck.part021 NeonCityRush.pck
```

**macOS / Linux：**

```sh
cat NeonCityRush.pck.part* > NeonCityRush.pck
```

把 `NeonCityRush.exe` 和合并后的 `NeonCityRush.pck` 放在同一目录，双击 exe 即可游玩，无需安装。

配置要求：支持 Vulkan 的显卡（大致 GTX 900 / RX 400 / Intel UHD 620 及以上）。首次启动会编译着色器，卡顿数十秒属于正常现象。

### 校验值（SHA-256）

| 文件 | SHA-256 |
| --- | --- |
| NeonCityRush.pck（合并后） | `544b5fd40e9274fd8ab8339db87163edd9017395bcfc73a8f55bd86d469bdf1f` |
| NeonCityRush.exe | `d34d36f3be1a6c49c56525ae86469b92e4f417ddf0b43cf00dd80c385c4b0562` |

## 操作

- WASD 移动 / 转向，鼠标看视角，Shift 冲刺，空格 跳 / 手刹
- F 上车 / 下车，Esc 暂停
- 对话：回车或鼠标左键继续；Tab 跳过过场
- F3：开关 FPS 面板

## 已知问题

- 本包未做「关闭窗口」实机验收，关窗时可能短暂卡住，稍等或结束进程即可
- 默认 boot_safe 低画质稳妥模式；进阶用户可加启动参数 `--no_boot_safe` 走完整画质路径
- 画面密度与外观仍在迭代，未达最终参考图水准

更多说明见仓库内 [玩法说明.txt](玩法说明.txt)。