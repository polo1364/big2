# v16：修正「牌點不到」
**原因**：先前把 `.player` 設成 `pointer-events:none`，導致其子層（手牌 `.hand`）也吃不到點擊。  
**解法**：移除 `pointer-events:none`，並確保 `.hand{pointer-events:auto}`。另外保留「拖曳多選」與加大的命中區域。

如果你的裝置仍有點擊問題，請回覆「手機型號＋瀏覽器版本」，我會對該裝置再加專用斷點與事件 fallback（如 touchstart）。
