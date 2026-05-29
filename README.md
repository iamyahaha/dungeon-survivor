# 地牢幸存者 · Dungeon Survivor

一个《吸血鬼幸存者》风格的网页肉鸽小游戏。自动攻击逼近的怪物，吃经验晶石升级，每次升级三选一变强，看你能活多久。

## 在线试玩
👉 部署后这里会是你的 GitHub Pages 链接

## 玩法
- **电脑**：`WASD` / 方向键移动，`P` 或 `Esc` 暂停
- **手机**：屏幕上拖动移动，点右上角 ⏸ 暂停
- 武器全自动开火，你只需走位、吃晶石、升级

## 本地运行
直接用浏览器打开 `index.html` 即可，或起一个静态服务器：

```bash
python3 -m http.server 8000
# 然后浏览器访问 http://localhost:8000
```

## 文件说明
- `index.html` — 游戏本体（HTML + Canvas + JS，单文件）
- `hero.png` — 主角精灵图集（4 帧）
- `grub.png` / `runner.png` — 普通小怪精灵图集（4 帧）
