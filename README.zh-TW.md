<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="bestimage.ai 標誌"></a></p>

# Wan 3.0 影片提示詞精選庫｜繁體中文指南

**14 個分類、148 個影片創作簡報**。

[英文首頁](README.md) · [簡體中文](README.zh-CN.md) · [全部 15 種語言](locales/README.md) · [完整場景索引](prompts/README.md)

![概念畫面：晨光中的天文台圖室，檔案管理員展開星圖](assets/wan-3-prompt-collection-hero.png)

*這是內建圖像生成工具製作的靜態概念圖，並非 Wan 3.0 影片輸出。請參閱[圖片提示詞與來源](assets/README.md)。*

## 內容範圍與開始方式

15 種語言提供在地化入口指南及同一條完整對照提示詞，**不代表全部 148 條案例均已翻譯**。前 6 類簡報為中文，後 8 類為英文；對照提示詞與譯文不另外計入案例數量。

從索引選擇簡報，調整細節並準備素材。參考素材的說明代表用途，不代表本庫已提供檔案。在所選入口設定時長、畫面比例、解析度與聲音；只在提示詞中寫參數不會設定 API 請求。先進行少量試作，再檢查動作、幾何結構、人物身分、時序及聲音。

## 八層提示詞結構

```text
[輸出] 時長 + 畫面比例 + 視覺媒介
[主體] 固定身分特徵 + 服裝或材質 + 不可改變的細節
[環境] 時間 + 地點 + 天氣 + 空間層次
[動作] 起因 → 連續動作 → 可見結果
[攝影機] 景別 + 機位 + 單一移動路徑 + 結束構圖
[視覺] 光線 + 色彩 + 質感 + 動態模糊
[聲音] 環境音 + 動作音 + 音樂 + 對白語言（平台支援時）
[限制] 必須保持的內容 + 需要避免的問題
```

## 完整對照提示詞

**模式：**文字生成影片 · **設定：**10 秒、16:9、開啟聲音 · **輸入素材：**無

```text
製作一個 10 秒、16:9 的紀錄片鏡頭，地點是安靜的社區工具借用室。一位留短捲髮的成年志工穿著芥末黃色圍裙和捲起袖子的海軍藍襯衫，在小型紅色桌扇始終拔掉插頭的狀態下進行維修。0–3 秒，志工把拆下的防護網罩放在靜止的桌扇旁。3–7 秒，用軟布擦去一片扇葉上的灰塵，同時攝影機在桌面高度緩慢向右平移。7–10 秒，放下軟布，將網罩對準外殼，不插電，也不啟動桌扇。窗外光線呈現磨損金屬與棉布的質感。聲音：布料擦拭聲、網罩一次輕輕的喀噠聲、安靜的室內環境音；無對白、無音樂。保持同一個人物、同一台風扇、三片扇葉、紅色外殼，以及始終未插電的電源線。不出現轉動的扇葉、額外工具、可讀標籤、字幕或剪接。
```

**可調變數：**圍裙顏色、桌扇顏色、室內光線。**檢查目標：**桌扇始終未插電且靜止；扇葉數量與手部接觸關係一致。這是創意場景，不是電器維修指引。

## bestimage.ai 的四種 Wan 3.0 API 用途

| 入口（英文模型頁） | 準備與檢查重點 |
|---|---|
| [文字生成影片](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | 完整描述一個事件的起因、動作與可見結果 |
| [圖片生成影片](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | 此平台的文件要求首圖**和尾圖**；交代過渡並固定構圖與結構 |
| [參考素材生成影片](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | 為人物、物體、空間、動作或聲音參考各指定一項明確用途 |
| [影片編輯](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | 提供原始影片與一項限定修改；其餘表演、時長、鏡頭和區域保持不變 |

模型頁提供目前的操作介面及公開請求範例。不同 Wan 產品未必提供相同設定；請參閱[能力與限制](guides/model-capabilities.md)。

[API 工作流程與成本控制指南](guides/bestimage-wan-3-api.md)使用英文，涵蓋請求、輪詢、輸入驗證與試作規劃。**bestimage.ai 的 API 主機為 `https://api.flaq.ai`。** 請使用在 bestimage.ai 帳號中取得的 API 金鑰。消耗額度前，請查看模型頁與帳號中的最新價格及使用條件。

## GPT Image 2：先準備參考畫面

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/)生成靜態圖片；[GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/)編輯圖片並結合視覺參考。可先準備角色設定圖、產品參考或核准的首尾構圖，檢查後再交給相應 Wan 入口。

這是**獨立圖像模型**，不是 Wan 影片介面。本庫不自動串接兩者，也不聲稱概念圖由這些 API 生成。請參閱[參考畫面工作流程](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow)。

## 指南與貢獻

[提示詞指南](guides/prompting-guide.md)、[能力指南](guides/model-capabilities.md)及[疑難排解](guides/troubleshooting.md)為簡體中文，API 指南為英文；未宣稱所有指南均有翻譯。完整分類與數量見[英文首頁](README.md)或[簡體中文首頁](README.zh-CN.md)。

分享前請閱讀[貢獻指南](CONTRIBUTING.md)或[簡體中文投稿說明](CONTRIBUTING.zh-CN.md)。提供準確設定、素材用途、使用權、觀察結果及真實的已測或未測狀態；不要分享憑證、私人文件或會過期的簽名媒體網址。

## 關於 bestimage.ai

本提示詞庫由 [bestimage.ai](https://bestimage.ai/) 團隊整理與維護，將實用創作流程與圖像、影片模型 API 連結起來。

## 加入 bestimage.ai 聯盟推廣計畫

製作教學、分享提示詞或發布 API 整合案例？加入 [bestimage.ai 聯盟推廣計畫](https://bestimage.ai/affiliate-program/)，向你的受眾推薦 bestimage.ai，並獲得推薦佣金。

- 受推薦使用者的首筆有效付費訂單，佣金為 **20%**。
- 該使用者**註冊後 60 天內**的後續有效付費訂單，佣金為 **10%**。

訂單資格與結算以[現行聯盟協議](https://bestimage.ai/affiliate-agreement/)為準。

## 授權條款

[MIT](LICENSE).
