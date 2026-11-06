# miniprogram-fonts

静态字体托管（仅文件，无业务后端）：为微信小程序「练习纸生成器」提供霞鹜文楷
LXGW WenKai 子集字体的网络加载源（wx.loadFontFace）。

## 文件

| 文件 | 说明 |
|---|---|
| `LXGWWenKai-Regular.subset.woff2` | 主源：6774 字子集（GB2312 常用字 + 项目字典追加），1,540,812 字节，sha256 前缀 ac1dfae4be8d0943 |
| `LXGWWenKai-Regular.subset.woff` | 低版本 iOS 备选：同字集 WOFF 格式，2,085,440 字节，sha256 前缀 349e512085293c7a |
| `OFL.txt` | 字体授权全文（SIL Open Font License 1.1） |

字体来源：LXGW WenKai v1.530（https://github.com/lxgw/LxgwWenKai），
子集由 fontTools 从官方 TTF 按项目字符集裁剪，未改字形。
OFL 附加条款允许子集化/格式转换后作 web font 分发（见 OFL.txt）。

## 部署（GitHub Pages）

仓库根目录即站点根目录，开启 Pages（main 分支 / root）后文件地址为：

- https://julytian.github.io/miniprogram-fonts/LXGWWenKai-Regular.subset.woff2
- https://julytian.github.io/miniprogram-fonts/LXGWWenKai-Regular.subset.woff

小程序侧地址常量在应用 `src/lib/font.ts` 的 `FONT_HOST_BASE`，上线切腾讯云 COS 时只改该常量。
