# IPTV 直播源合集（内蒙古联通 · 用户自用）

本仓库存放个人使用的 IPTV 直播源列表（m3u）。**推荐用国内可直连的镜像地址订阅。**

---

## 📺 订阅链接（复制到 APTV / TiviMate / Kodi 等）

| 文件 | 内容 | 订阅链接 |
|---|---|---|
| **`result.m3u`** ⭐ | **78 台**（本机实测有效的 IPv4 频道） | `https://gh-proxy.com/https://raw.githubusercontent.com/q122839552/iptv/main/result.m3u` |
| `iptv-api.m3u` | 131 台（含中国香港/中国澳门/中国台湾地区频道） | `https://gh-proxy.com/https://raw.githubusercontent.com/q122839552/iptv/main/iptv-api.m3u` |
| `nmg-iptv.m3u` | 128 台（内蒙古联通 IPTV 组播源，**需先搭 udpxy**） | `https://gh-proxy.com/https://raw.githubusercontent.com/q122839552/iptv/main/nmg-iptv.m3u` |

> 备选 CDN 写法：`https://fastly.jsdelivr.net/gh/q122839552/iptv@main/文件名`

---

## 🧩 链接是怎么来的（自助拼接规则）

订阅链接不用"生成"，是**拼出来的**，记住这个公式：

```
① GitHub 原始地址：
   https://raw.githubusercontent.com/{用户名}/{仓库}/{分支}/{文件名}

② 套上国内能直连的镜像：
   https://gh-proxy.com/{第①步那一整串}
```

本仓库的参数：用户名 `q122839552`、仓库 `iptv`、分支 `main`。所以任意文件的链接就是：

```
https://gh-proxy.com/https://raw.githubusercontent.com/q122839552/iptv/main/【文件名】
```

**换个文件名就行**，以后放任何新文件进去都能自己拼出链接。

---

## 🔄 怎么自己更新文件（不用求人）

**关键：链接永远不变！只需要替换文件内容。**

在 GitHub 网页上（电脑 / 手机都行）：

1. 打开仓库 → **点进要更新的文件**（如 `result.m3u`）
2. 点右上角 **铅笔图标 ✏️（Edit）**
3. 在编辑框里 **Ctrl+A 全选 → 删除 → 粘贴新内容**
4. 页面底部填提交说明 → 点 **Commit changes（提交更改）**
5. 完事！**链接一个字没变**，APTV 那边刷新订阅即可拿到新列表

---

## ⏱️ 多久更新一次

- 公网源**不必每天更新**，**2～3 天一次**即可；
- 央视、卫视等大台较稳；冷门台/地方台容易失效；
- **最省事的做法**：平时不管，等发现卡顿、黑屏变多时再跑一次；
- 想自动化：用桌面端 IPTV-API 的「定时任务」功能（需电脑常开）。

---

## ⚠️ 关于 `nmg-iptv.m3u`（内蒙古联通组播源）

它画质最好，但有**两个硬前提**：

1. **必须开通联通的 IPTV 业务**（组播数据只在专门的 IPTV VLAN 内）；
2. **必须自己搭「组播转单播」**（udpxy / msd_lite），并把文件里的 `192.168.1.100:4022` 换成自己的地址。

未满足以上条件时，订阅它只会显示频道列表、**无法播放**。

---

## 📌 说明

- 台标（频道图标）来自开源项目 [fanmingming/live](https://github.com/fanmingming/live)，经 jsDelivr 加速。
- 列表由 [Guovin/iptv-api](https://github.com/Guovin/iptv-api) 工具采集 / 校验 / 测速后生成。
- 公网源随时可能失效，结果不保证长期稳定。

---

## 📣 声明

- 本仓库仅供个人学习与测试使用。
- 请仅观看你已获得合法授权的内容，遵守《广播电视管理条例》等当地法律法规。
- 请勿用于传播、转发或公开分发未经授权的直播源。
