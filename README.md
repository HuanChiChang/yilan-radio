# 爸爸的收音機（宜蘭）

> 最後更新：2026-10-11

給爸爸在手機上聽廣播的網頁 App（PWA）。不用上架、不用安裝商店 App，手機瀏覽器打開後「加到主畫面」就像一般 App。

## 功能

- 字很大、按鈕很大，點電台名稱就播放，底部大圓鈕停止 / 播放
- **中原電台**固定在最上方，用金色大卡片特別標示（找不到串流時會顯示說明）
- 宜蘭在地電台（宜蘭、蘭陽、噶瑪蘭、羅東…）排最前面，再來是警廣、中廣、教育、漢聲、央廣等
- ☆ 加入「我的最愛」，最愛會顯示在最上面
- 記得上次聽的電台
- 鎖定畫面可以控制播放（Media Session）
- 電台清單來自 [Radio Browser](https://www.radio-browser.info/) 公開資料庫，每次打開自動更新；網路不穩時用上次的清單

## 怎麼放上網路（建議：GitHub Pages）

需要 **https** 網址，手機才能安裝成 App。

1. GitHub repo → Settings → Pages
2. Source 選 `Deploy from a branch`，分支選放這個資料夾的分支，資料夾選 `/ (root)`
3. 網址會是 `https://huanchichang.github.io/yilan-radio/`

> 注意：GitHub Pages 對私人 repo 需要付費方案；也可以把這個資料夾單獨放到一個公開 repo，或丟到 Netlify / Cloudflare Pages（直接拖拉資料夾即可）。

## 在爸爸手機上安裝

- **Android（Chrome）**：打開網址 → 右上角 ⋮ → 「加到主畫面」/「安裝應用程式」
- **iPhone（Safari）**：打開網址 → 下方分享按鈕 → 「加入主畫面」

## 本機測試

```bash
cd yilan-radio
python3 -m http.server 8000
# 打開 http://localhost:8000
```

## 已知限制

- https 網頁不能播放 http 開頭的串流，所以這類電台會自動隱藏
- 部分電台（例如中廣、飛碟）的官方串流可能沒有收錄在 Radio Browser，或網址會變動；找不到想聽的電台時，可以到 Radio Browser 網站新增或回報
