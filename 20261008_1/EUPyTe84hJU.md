# Enter 過後：一個網頁的旅程

- 影片 ID：EUPyTe84hJU
- 時長：13:29
- 來源：https://www.youtube.com/watch?v=EUPyTe84hJU
- 逐字稿：YouTube 手動 zh-TW 字幕

## 一句話總結
以科普方式拆解「在瀏覽器輸入 URL 按 Enter 之後發生什麼」，涵蓋網路分層、DNS、TCP/TLS 到網頁渲染與資安。

## 內容重點
- TCP/IP 四層抽象：應用層、傳輸層（Port）、網路層（IP、NAT）、連結層（MAC、ARP）。
- 送出請求：DNS 解析（層層詢問根／TLD／權威伺服器）→ TCP 三向交握 → TLS 握手（加密與憑證驗證）→ HTTP GET。
- 回應：Status Code（2/3/4/5 開頭意義）；抓取 CSS／JS／圖片。
- 渲染：HTML→DOM、CSS→CSSOM、合成 Render tree、Layout 排版、繪製像素；JS 觸發重排重繪。
- 演進：HTTP/2 共用 TCP 連線、HTTP/3 改用 QUIC（UDP）。
- 資安：中繼節點可讀改封包；HTTPS 加密必要；網路戰與假訊息是現代信任危機。

## 一句話
「短短幾秒的背後，是無數運算與協定共同完成的接力賽。」
