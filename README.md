# 风鸢五笔（kite-wubi）

基于极点五笔的五笔类形码。  
基本与五笔86相同，但用算法降低码长。  
当前还在开发，可能后续有破坏性的更新。  

## 和86有什么区别？
### 声母识别码
对于不满三码的字，末尾补声母识别码

翘舌音使用双拼
零声母取韵母首位  

```plain
sh -> u
ch -> i
zh -> v
ou ->o  
ang -> a  
....

特别地 z=v
```
## 简码重分配
用算法分配简码。  

对于字频表加权后的平均码长（不含上屏键）  
五笔86：2.32 每字  
风鸢五笔：2.06 每字  
# 安装

1. 把 `rime/` 里的**所有文件**拷进 Rime 用户目录：
   | 平台 | 目录 |
   |---|---|
   | Windows（小狼毫） | `%APPDATA%\Rime` |
   | macOS（鼠须管） | `~/Library/Rime` |
   | Linux（ibus-rime） | `~/.config/ibus/rime` |
   | Linux（fcitx5-rime） | `~/.local/share/fcitx5/rime` |

2. 重新部署（托盘菜单 → 重新部署）。
3. 按 `F4` 选「**风鸢五笔**」。

> 已经有 `default.custom.yaml` 的话，**别整个覆盖**，只把 `schema_list` 里的
> `- schema: kite_wubi` 那一行并进去。

## 许可 && 鸣谢

Apache License 2.0，见 `LICENSE`。

* 全码来自 [KyleBing/rime-wubi86-jidian](https://github.com/KyleBing/rime-wubi86-jidian), Apache 2.0
* 单字简码由[Killian2026/chu-jian-rang-quan](https://github.com/Killian2026/chu-jian-rang-quan)求解器算出。
* [邢红兵 25亿字语料汉字字频表](https://faculty.blcu.edu.cn/xinghb/zh_CN/article/167473/content/1437.htm) 本项目使用了这个字频。
