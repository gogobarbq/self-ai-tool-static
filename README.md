# NC Blogger Toolkit v0.9

這個版本包含彼此配套的兩支工具。

## 1. blogger-theme-workbench.html

用途：修改 Blogger Theme。

這一版可安裝：

- NC Accordion 的 CSS 與 JavaScript
- YouTube iframe 的 16:9 響應式 CSS

建議先使用這支工具載入目前 Blogger Theme，勾選需要的文章元件，再輸出完整 Theme XML 並套用至 Blogger。

## 2. nc-markdown-compiler.html

用途：將 Obsidian／Markdown 內容轉成適合 StackEdit → Blogger 的內容。

目前支援：

- `{{img:tag}}`
- `{{note}} ... {{end}}`
- `{{warning}} ... {{end}}`
- `{{accordion title="更多背景"}} ... {{end}}`
- `{{reference}} ... {{end}}`
- Markdown hyperlink 另開新視窗
- 裸網址轉 hyperlink
- YouTube 網址轉 iframe，保留全螢幕功能

## 建議使用順序

1. 使用 Theme Workbench 更新並套用 Blogger Theme。
2. 使用 NC Markdown Compiler 產生文章內容。
3. 將結果貼到 StackEdit，檢查後發布至 Blogger。

## 本次相容性處理

StackEdit 可能移除文章 HTML 中的 wrapper class 與 inline style。

因此：

- Accordion 使用 Blogger 較容易保留的 `div`／`button` 結構。
- YouTube 由 Theme 直接辨識 `iframe[src*="youtube.com/embed"]`，不依賴外層 class 或 inline style。
