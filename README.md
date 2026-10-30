# 雾里楼台 · 文集

日记、随感、长文。研墨落笔，收墨藏稿。

线上：<https://kinghihido.github.io/wuliloutai-writing/>

## 这是原来那个

这个站的前身是「集大成者」总台里的 `writing.html`。那一版在重构总台时被删掉了，这是从 git 历史里
（`jidacheng` 的 `02f0ba99`）完整捞回来后独立成站的，内容一字未改。

## 稿件存在哪

**存在你自己浏览器的 localStorage 里**，键名 `jdc.writings`。

这一点很重要，两个后果：

- 换设备、换浏览器、清缓存 → 稿子不会跟着走。站里也写了这句提醒。
- 好消息是：新站和总台同在 `kinghihido.github.io` 这个域下，**存储键也沿用了同一个**。
  所以你在旧总台里写过的东西，打开这个站会自动出现在「藏稿」里，不用迁移。

想备份的话，控制台里跑一句，把输出存成文件：

```js
copy(localStorage.getItem("jdc.writings"))
```

恢复则反过来：

```js
localStorage.setItem("jdc.writings", "<粘贴刚才的内容>")
```

## 结构

单文件站点，没有构建步骤，没有后端：

```
index.html   全部内容：结构、样式、交互都在这一个文件里
```

打开方式：起个静态服务（`file://` 直接打开会被浏览器拦 localStorage）：

```bash
python -m http.server 8000
```

## 页面里有什么

- **入站过渡页** — WebGL2 流体墨染水面，点一下墨落生漪，再点「入燕园」渐显进正文
- **研墨** — 写作区。题目留空自动取正文首句，体裁分日记 / 随感 / 长文，实时字数
- **藏稿** — 列表。点题名展卷细读，可调出续写；盖印后显示收墨时辰
- **时辰 / 诗签** — 右上角传统时辰，页首随机一句古诗
- **落花** — 右下角开关，飘落花瓣

## 视觉

水墨的雾绿纸感：纸 `#e9eee8`，墨 `#1b2b2a`，松绿 `#2f4a45`，印章朱砂 `#9a4a3a`。
字体是 Ma Shan Zheng + Noto Serif SC。

## 相关

| 站 | 主色 | 内容 |
| --- | --- | --- |
| [层林尽染](https://github.com/kinghihido/wuli-loutai) | 朱砂红 | 技术流，三篇 |
| [学海无涯](https://github.com/kinghihido/paper-reading) | 苍蓝 | 文献精读，22 篇报告 |
| [燕园](https://github.com/kinghihido/yanyuan-poi) | 雾绿 | 北大校内 POI 地图 |
| **雾里楼台**（本仓库） | 雾绿 | 文集 |
| [集大成者](https://github.com/kinghihido/jidacheng) | 墨 | 总台 |
