# 六個介面：需求、線稿 Prompt 與 Stitch Prompt

本文件供「我想說這句｜Say This」課堂原型使用。流程為：先用「線稿 Prompt」生成低擬真 wireframe，確認資訊層級與操作順序；再將同一頁的「Stitch Prompt」貼到 Stitch 生成高擬真手機介面。

## 共用設計規則

六個介面必須像同一款 App，請在每次生成時維持以下設定：

- 裝置：手機直式介面，基準尺寸 390 × 844 px。
- 使用者：18 歲以上華語英文學習者，視覺成熟、友善，不兒童化。
- 語言：介面使用繁體中文；英文只出現在學習內容與必要標籤。
- 主色：靛藍 `#5B5BD6`；輔色：青綠 `#28B8A6`。
- 背景：帶冷色的淺灰白 `#F7F8FC`；主文字：深藍黑 `#172033`。
- 字體：Noto Sans TC 搭配 Inter；標題清楚、內文易讀。
- 元件：16 px 圓角卡片、細邊框、輕微陰影、充足留白。
- 按鈕：主要按鈕使用靛藍實心、白字；次要按鈕使用白底描邊。
- 圖示：簡潔線性圖示，不使用 emoji、照片、3D 人物或大型裝飾插圖。
- 操作：觸控區至少 44 px；重要文字維持高對比。
- 導覽：主要功能頁底部使用「首頁／句子庫／複習」三項導覽；程度設定頁不顯示底部導覽。
- 文案語氣：直接、溫和、不責備，不使用遊戲化幼稚語氣。

---

## 介面一：英文程度設定

### 介面任務

第一次使用時，讓使用者用白話說明選擇程度。這一頁不是考試，也不要求使用者理解 A1、B1、C1；CEFR 代號只作補充。選擇後成為之後推薦英文版本與解析深度的依據。

### 必要內容

- 品牌名稱「我想說這句」與一句簡短說明。
- 標題：「你的英文目前比較接近哪一種？」
- 補充：「不用擔心，之後可以隨時調整。」
- 三張單選卡：入門／中階／進階。
- 每張卡包含白話能力描述與較小的 CEFR 參考標籤。
- 未選擇時主要按鈕停用；選擇後按鈕「開始使用」啟用。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，產品是成人英文學習 App「我想說這句」。這是第一次使用的英文程度設定頁。

只使用黑、白、灰與線框，不加入正式配色、插圖、照片或陰影。畫面頂部放小型品牌名稱「我想說這句」，中上方放主標題「你的英文目前比較接近哪一種？」及輔助文字「不用擔心，之後可以隨時調整。」

主內容垂直排列三張大型單選卡：
1. 入門｜A1–A2｜能理解常見單字與簡單句子，希望先把意思說清楚。
2. 中階｜B1–B2｜能應付日常對話，希望說得更自然、完整。
3. 進階｜C1 以上｜能理解複雜內容，希望掌握細微語氣與精準用法。

每張卡左側有單選圓鈕，選取狀態要明確。畫面底部固定一個全寬主要按鈕「開始使用」。此頁不要放底部導覽。資訊層級清楚，卡片可單手點擊，避免任何裝飾性內容。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile app screen for a Traditional Chinese adult English-learning product named「我想說這句｜Say This」. Screen size 390×844 px, portrait. This is the first-time English level selection screen.

Use Traditional Chinese UI copy. The visual style is calm, trustworthy, modern, and encouraging for adults—not playful or childlike. Use a cool off-white background #F7F8FC, deep navy text #172033, indigo primary #5B5BD6, teal accent #28B8A6, Noto Sans TC with Inter, 16px rounded cards, subtle borders and soft shadows. Do not use photos, emojis, mascots, 3D illustrations, or strong gradients.

Layout:
- Small brand lockup at top:「我想說這句」and small English label “Say This”.
- Large heading:「你的英文目前比較接近哪一種？」
- Supporting text:「不用擔心，之後可以隨時調整。」
- Three stacked selectable cards with radio controls:
  1.「入門」badge “A1–A2”; description「能理解常見單字與簡單句子，希望先把意思說清楚。」
  2.「中階」badge “B1–B2”; description「能應付日常對話，希望說得更自然、完整。」
  3.「進階」badge “C1 以上”; description「能理解複雜內容，希望掌握細微語氣與精準用法。」
- Show「中階」as the selected example with a clear indigo border, tinted background, and selected radio.
- Sticky bottom primary button:「開始使用」.

No bottom navigation on this screen. Keep touch targets at least 44px and maintain strong contrast and generous spacing.
```

---

## 介面二：輸入首頁

### 介面任務

讓使用者在最少步驟內完成一句中文、情境與語氣設定。英文程度沿用個人設定，只在頁面上顯示可調整的程度標籤，避免每次重選。

### 必要內容

- 問候與目前程度標籤，例如「中階 B1–B2」。
- 大型中文輸入框，提示「你現在想用英文說什麼？」
- 範例文字：「我今天工作很多，可能會晚一點下班。」
- 情境選擇：日常／工作／旅行／社交。
- 語氣選擇：自然／正式／禮貌／輕鬆。
- 主要按鈕：「看看英文怎麼說」。
- 底部導覽：首頁／句子庫／複習。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，這是成人英文學習 App「我想說這句」的首頁輸入畫面。只使用黑白灰線框，不使用正式配色、圖片、插圖或裝飾。

頂部左側放問候「今天想說什麼？」；右側放可點擊的程度標籤「中階 B1–B2」。下方放一個佔畫面主要空間的大型多行輸入框，標籤為「你現在想用英文說什麼？」，框內示範「我今天工作很多，可能會晚一點下班。」並在右下角顯示字數。

輸入框下方依序放：
- 情境區，四個可選按鈕：日常、工作、旅行、社交；工作為選取示例。
- 語氣區，四個可選按鈕：自然、正式、禮貌、輕鬆；自然為選取示例。

靠近底部放全寬主要按鈕「看看英文怎麼說」。最底部放三項導覽：首頁、句子庫、複習，首頁為選取狀態。資訊順序必須是輸入內容、情境、語氣、送出，不要加入歷史紀錄、廣告或其他次要功能。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile home screen, 390×844 px portrait, for the Traditional Chinese adult English-learning app「我想說這句｜Say This」. The goal is to help a user enter a real-life Chinese sentence, choose context and tone, and generate level-appropriate English.

Use the shared visual system: off-white #F7F8FC background, deep navy #172033 text, indigo #5B5BD6 primary, teal #28B8A6 accent, Noto Sans TC + Inter, 16px rounded cards, subtle borders and soft shadows. Mature and friendly, not childlike. No photos, emojis, mascots, 3D assets, or large decorative illustrations.

Layout:
- Header left: heading「今天想說什麼？」and small supportive subtitle「把生活中的一句話，變成真正會用的英文。」
- Header right: tappable outlined level chip「中階 B1–B2」with a small chevron.
- Large multiline input card labeled「你現在想用英文說什麼？」. Show sample input「我今天工作很多，可能會晚一點下班。」and a small character count at lower right.
- Section label「使用情境」with four compact selectable chips: 日常、工作、旅行、社交. Show「工作」selected.
- Section label「表達語氣」with four chips: 自然、正式、禮貌、輕鬆. Show「自然」selected.
- Full-width indigo primary button「看看英文怎麼說」with a simple arrow icon.
- Bottom navigation with three items and line icons:「首頁」「句子庫」「複習」. Home is active in indigo.

Prioritize the text input as the visual hero. Use clear labels, 44px minimum touch targets, keyboard-safe spacing, and no unnecessary dashboard widgets.
```

---

## 介面三：英文結果

### 介面任務

先提供一個清楚的推薦答案，再讓使用者切換其他難度。使用者不應一進頁面就看到大量文法內容；解析要透過次要操作進入。

### 必要內容

- 原始中文與情境／語氣標籤。
- 「推薦給你的說法」標籤。
- 一句大型英文結果。
- 基礎版／自然版／精準版切換。
- 每個版本的簡短定位，例如「最容易直接使用」。
- 聽發音、查看解析、收藏三個操作。
- 「重新調整條件」的文字操作。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，這是成人英文學習 App「我想說這句」的英文結果頁。只使用黑白灰線框，不加入正式配色、插圖或照片。

頂部有返回按鈕與標題「英文怎麼說」。先用小型卡片顯示原始中文「我今天工作很多，可能會晚一點下班。」以及小標籤「工作」「自然」「中階」。

主畫面中央是一張最醒目的結果卡：上方標籤「推薦給你的說法」，英文大字顯示“I have a lot on my plate today, so I might get off work a little late.”，下方顯示簡短中文與定位「日常工作場合自然、完整的說法」。英文右側或下方放播放發音按鈕。

結果卡下方放三段式切換：基礎版、自然版、精準版；自然版為選取狀態。再放兩個主要操作按鈕「查看解析」「收藏這句」，以及一個較弱的文字操作「重新調整條件」。底部保留首頁、句子庫、複習導覽。不要同時展開單字、文法和比較內容。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile result screen, 390×844 px portrait, for「我想說這句｜Say This」, a Traditional Chinese adult English-learning app. The screen should present one clear recommended English expression first and keep detailed teaching content secondary.

Use the shared visual system: #F7F8FC background, #172033 text, #5B5BD6 indigo primary, #28B8A6 teal accent, Noto Sans TC + Inter, 16px cards, subtle borders and soft shadows. Mature, calm, encouraging. No photos, emojis, mascots, 3D assets, flags, or decorative illustrations.

Layout:
- Top app bar with back arrow and title「英文怎麼說」.
- Compact source card showing Chinese text「我今天工作很多，可能會晚一點下班。」and small chips「工作」「自然」「中階」.
- Main elevated result card, visually dominant:
  - Small teal label「推薦給你的說法」.
  - Large English sentence: “I have a lot on my plate today, so I might get off work a little late.”
  - Small Traditional Chinese explanation「日常工作場合自然、完整的說法。」
  - Circular audio playback control with speaker icon and label「聽發音」.
- Segmented control below:「基礎版」「自然版」「精準版」, with「自然版」selected.
- Two clear actions: primary indigo button「查看解析」and secondary outlined button with bookmark icon「收藏這句」.
- Low-emphasis text action「重新調整條件」.
- Bottom navigation:「首頁」「句子庫」「複習」.

Do not show full vocabulary or grammar explanations on this page. Keep the recommended sentence as the hero and make version switching obvious but not visually noisy.
```

---

## 介面四：句子解析

### 介面任務

解釋英文為什麼這樣說，並把使用者最需要學的內容分成可消化的小區塊。內容深度依程度調整，但畫面不要像教科書或長篇文章。

### 必要內容

- 英文主句與播放發音。
- 重點片語：`have a lot on my plate`。
- 句型結構：原因＋結果。
- 語氣說明與適用情境。
- 與基礎版／精準版的差異比較，可收合。
- 收藏或開始練習的主要操作。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，這是成人英文學習 App「我想說這句」的句子解析頁。只使用黑白灰線框，不加入正式配色、插圖、照片或裝飾。

頂部有返回按鈕與標題「這句怎麼用」。最上方顯示完整英文句子“I have a lot on my plate today, so I might get off work a little late.”，句中重要片語用框線或底線標示，旁邊有播放發音按鈕。

內容以下列卡片垂直排列：
1.「重點片語」：have a lot on my plate，附中文意義與一個簡短使用說明。
2.「句型結構」：I have... today, so I might...，以原因→結果的方式說明。
3.「語氣與場合」：標示自然、工作、口語，說明適合對同事或朋友使用。
4. 可收合的「看看其他說法」，比較基礎版與精準版，不預設全部展開。

頁面底部固定主要按鈕「開始練習」，旁邊或上方有次要按鈕「收藏這句」。底部不必重複主導覽，以免與固定操作衝突。不要把解析做成密集長文。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile learning explanation screen, 390×844 px portrait, for the Traditional Chinese adult English-learning app「我想說這句｜Say This」. The screen explains why one English expression works without looking like a dense textbook.

Use the shared visual system: cool off-white #F7F8FC, deep navy #172033, indigo #5B5BD6, teal #28B8A6, Noto Sans TC + Inter, 16px rounded cards, subtle borders and soft shadows. Mature and calm. No photos, emojis, mascots, 3D illustrations, or decorative hero art.

Layout:
- Top app bar with back arrow and title「這句怎麼用」.
- Sentence header card containing: “I have a lot on my plate today, so I might get off work a little late.” Highlight “have a lot on my plate” with a soft teal background. Add a compact audio button「聽發音」.
- Stacked teaching cards with clear icons and short content:
  1.「重點片語」: “have a lot on my plate”／「手上有很多事要處理」／「比 have a lot of work 更口語自然。」
  2.「句型結構」: visually show「原因 I have...」→「結果 so I might...」.
  3.「語氣與場合」: chips「自然」「工作」「口語」and short note「適合對同事或朋友說明今天可能晚下班。」
  4. Collapsed accordion「看看其他說法」with a chevron and subtitle「比較基礎版與精準版」.
- Sticky bottom action area: primary button「開始練習」and secondary bookmark action「收藏這句」.

Keep paragraphs short, use progressive disclosure, and make highlighted learning points easy to scan.
```

---

## 介面五：我的句子庫

### 介面任務

讓使用者快速找回以前真正需要使用的句子，而不是變成無法整理的收藏牆。卡片需同時保留中文、英文、情境與熟悉度。

### 必要內容

- 搜尋欄。
- 篩選：全部／待複習／已熟悉；以及情境篩選。
- 句子卡：中文、英文、情境、語氣、熟悉度與下次複習。
- 卡片操作：查看、播放、更多選單。
- 空狀態與搜尋無結果狀態需有清楚引導。
- 底部導覽，句子庫為選取狀態。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，這是成人英文學習 App「我想說這句」的「我的句子庫」頁。只使用黑白灰線框，不加入正式配色、照片、插圖或裝飾。

頂部標題「我的句子庫」，右側顯示總數「12 句」。下方放全寬搜尋欄「搜尋中文或英文」。再放一列可橫向滑動的篩選：全部、待複習、學習中、已熟悉；全部為選取狀態。另有一個情境篩選按鈕。

內容以垂直卡片清單呈現，每張卡包含：
- 一行中文，例如「我今天工作很多，可能會晚一點下班。」
- 兩行內英文，例如“I have a lot on my plate today...”
- 小標籤「工作」「自然」
- 熟悉度標籤，例如「學習中」或「待複習」
- 下次複習資訊，例如「今天」
- 播放按鈕與更多選單

至少顯示三張不同狀態卡片。最底部放首頁、句子庫、複習導覽，句子庫為選取狀態。不要使用表格或密集列表。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile library screen, 390×844 px portrait, for the Traditional Chinese adult English-learning app「我想說這句｜Say This」. The goal is to help users find and review saved real-life English expressions.

Use the shared visual system: #F7F8FC background, #172033 text, #5B5BD6 primary, #28B8A6 accent, Noto Sans TC + Inter, rounded 16px cards, light borders and soft shadows. Mature, calm, and highly readable. No photos, emojis, mascots, 3D art, or decorative illustrations.

Layout:
- Header title「我的句子庫」and small count「12 句」.
- Full-width search field with search icon and placeholder「搜尋中文或英文」.
- Horizontally scrollable filter chips:「全部」「待複習」「學習中」「已熟悉」, with「全部」selected. Add a separate filter button「情境」with sliders icon.
- Vertical list of three saved sentence cards. Each card contains:
  - Chinese source sentence.
  - English sentence limited to two lines.
  - Context and tone chips such as「工作」「自然」.
  - Familiarity status such as「待複習」「學習中」「已熟悉」using accessible color plus text, not color alone.
  - Small next-review text such as「今天複習」or「3 天後」.
  - Compact audio icon and overflow menu.
- Bottom navigation with「首頁」「句子庫」「複習」, sentence library active in indigo.

Make cards easy to scan and tap. Avoid tables, crowded metadata, streaks, scores, or gamified badges.
```

---

## 介面六：句子複習

### 介面任務

讓使用者主動回想收藏的句子，而不是再看一次答案。第一版以中翻英為主，作答後再顯示正確答案與解析；錯題會重新排入複習。

### 必要內容

- 今日進度，例如 2／5。
- 題目中文與情境提示。
- 英文輸入框。
- 「送出答案」主要按鈕。
- 答題後狀態：正確／需要再練習。
- 正確答案與差異提示。
- 自評：還不熟／有點熟／已熟悉。
- 底部導覽，複習為選取狀態。

### 線稿 Prompt

```text
請設計一張手機直式低擬真線稿，尺寸比例約 390×844，這是成人英文學習 App「我想說這句」的中翻英複習頁。只使用黑白灰線框，不加入正式配色、插圖、照片或裝飾。

頂部左側放關閉按鈕，中央顯示「今日複習」，右側顯示「2／5」。下方放細長進度條。

主要題目卡顯示：
- 情境標籤「工作｜自然」
- 提示「請試著用英文說：」
- 大字中文「我今天工作很多，可能會晚一點下班。」

題目卡下方放大型英文多行輸入框，提示「輸入你的英文句子」。接著放全寬主要按鈕「送出答案」。在畫面下半部預留答題回饋區，標示送出後會顯示「正確答案」「你的答案差異」與三個自評按鈕「還不熟／有點熟／已熟悉」。

底部放首頁、句子庫、複習導覽，複習為選取狀態。此張線稿以未作答狀態為主，不要提前顯示答案。
```

### Stitch Prompt

```text
Create one polished high-fidelity mobile review screen, 390×844 px portrait, for the Traditional Chinese adult English-learning app「我想說這句｜Say This」. This is an active recall exercise: the user sees Chinese and must produce the English sentence before seeing the answer.

Use the shared visual system: #F7F8FC background, #172033 text, #5B5BD6 indigo primary, #28B8A6 teal accent, Noto Sans TC + Inter, 16px cards, subtle borders and soft shadows. Mature and supportive, never childish or punitive. No photos, emojis, mascots, 3D assets, confetti, streak flames, or game-score visuals.

Layout:
- Top row: close icon, centered title「今日複習」, progress text「2／5」.
- Thin progress bar below, 40% complete.
- Main prompt card with small chips「工作」「自然」, label「請試著用英文說：」and large Chinese sentence「我今天工作很多，可能會晚一點下班。」
- Large multiline answer field with placeholder「輸入你的英文句子」and a small optional action「給我一個提示」.
- Full-width primary button「送出答案」.
- Show a collapsed preview area labeled「送出後會顯示答案與解析」; do not reveal the correct answer in this default state.
- Bottom navigation with「首頁」「句子庫」「複習」, review active in indigo.

Also define visual states for later implementation: correct uses teal with text「答對了」; incorrect uses warm amber, not red, with text「再練一次就會更熟」. After submission, show the correct answer, highlight meaningful differences, and offer three self-rating buttons「還不熟」「有點熟」「已熟悉」.
```

---

## 建議的生成順序

1. 先生成「輸入首頁」，確認整體品牌與元件風格。
2. 再生成「英文結果」與「句子解析」，確認主要學習流程。
3. 接著生成「句子庫」與「句子複習」。
4. 最後生成「程度設定」，讓它沿用前面已確立的視覺系統。

每次送入 Stitch 時，如果工具能加入參考畫面，請把前一張已確認的畫面一併提供，並補充：「沿用同一套色彩、字體、按鈕、卡片、間距與底部導覽，不重新設計品牌風格。」

