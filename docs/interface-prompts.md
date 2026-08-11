# 六個介面：需求、線稿 Prompt 與 Stitch Prompt

本文件供「我想說這句｜Say This」課堂原型使用。老師要求的主要流程是：先用一個「六頁線稿總 Prompt」一次生成六張低擬真 wireframe；確認後，再用一個「六頁 Stitch 總 Prompt」一次生成六個一致的高擬真手機介面。後面的單頁 Prompt 只在某一頁需要補做或修正時使用。

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

## 一次生成六張：線稿總 Prompt

請將下面整段一次貼入線稿生成工具，不要拆成六次：

```text
請為手機 App「我想說這句｜Say This」一次產生完整的六頁低擬真線稿。這是一款給 18 歲以上華語英文學習者使用的產品：使用者輸入生活中真正想說的中文，系統依其英文程度、情境與語氣提供自然英文，接著協助理解、收藏與複習。

輸出要求：
- 一次輸出六張獨立的手機直式介面，不是同一頁的六種版本，也不是一張長頁面。
- 六張介面放在同一個設計板上，以 3×2 或 2×3 方式排列，每張手機框比例約 390×844。
- 每張畫面外側清楚標示編號與名稱：01 程度設定、02 輸入首頁、03 英文結果、04 句子解析、05 句子庫、06 句子複習。
- 只使用黑、白、灰與線框，呈現低擬真 wireframe；不要正式配色、照片、插圖、3D 圖像、漸層或裝飾。
- 六頁沿用同一套頁首、卡片、按鈕、欄位、標籤、字級與間距。
- 主要功能頁底部使用相同的「首頁／句子庫／複習」導覽；程度設定頁不顯示底部導覽。
- 強調操作順序與資訊層級，觸控元件大小合理，避免把所有資訊塞在同一頁。

01 程度設定：
- 品牌名稱「我想說這句」與標題「你的英文目前比較接近哪一種？」
- 輔助文字「不用擔心，之後可以隨時調整。」
- 三張大型單選卡：入門 A1–A2、中階 B1–B2、進階 C1 以上，每張都有白話能力描述。
- 中階為選取示例。
- 底部全寬按鈕「開始使用」，此頁沒有底部導覽。

02 輸入首頁：
- 頁首「今天想說什麼？」與可調整程度標籤「中階 B1–B2」。
- 大型多行輸入框「你現在想用英文說什麼？」；示範內容「我今天工作很多，可能會晚一點下班。」
- 情境選擇：日常、工作、旅行、社交，工作為選取狀態。
- 語氣選擇：自然、正式、禮貌、輕鬆，自然為選取狀態。
- 全寬按鈕「看看英文怎麼說」。
- 底部導覽首頁為選取狀態。

03 英文結果：
- 返回按鈕與標題「英文怎麼說」。
- 小卡顯示原始中文，以及「工作／自然／中階」標籤。
- 主要結果卡標示「推薦給你的說法」，大字顯示 “I have a lot on my plate today, so I might get off work a little late.”
- 發音播放按鈕。
- 三段切換：基礎版、自然版、精準版，自然版為選取狀態。
- 操作「查看解析」「收藏這句」與文字連結「重新調整條件」。

04 句子解析：
- 返回按鈕與標題「這句怎麼用」。
- 顯示完整英文句子，框選重點片語 “have a lot on my plate”，並有發音按鈕。
- 三張解析卡：重點片語、句型結構、語氣與場合。
- 一個收合區「看看其他說法」。
- 底部固定主要按鈕「開始練習」與次要操作「收藏這句」。
- 避免密集長文，不顯示底部主導覽。

05 句子庫：
- 標題「我的句子庫」與數量「12 句」。
- 搜尋欄「搜尋中文或英文」。
- 篩選：全部、待複習、學習中、已熟悉，以及情境篩選。
- 三張句子卡，每張有中文、兩行內英文、情境與語氣標籤、熟悉度、下次複習時間、播放與更多操作。
- 底部導覽句子庫為選取狀態。

06 句子複習：
- 頁首「今日複習」、進度「2／5」與進度條。
- 題目卡顯示「工作／自然」、提示「請試著用英文說：」及中文句子「我今天工作很多，可能會晚一點下班。」
- 大型英文輸入框「輸入你的英文句子」。
- 次要操作「給我一個提示」與主要按鈕「送出答案」。
- 未作答狀態不要提前顯示正確答案；預留送出後答案與解析區。
- 底部導覽複習為選取狀態。

請讓六張線稿明確構成同一條使用流程：程度設定 → 輸入中文 → 查看英文結果 → 理解句子 → 收藏到句子庫 → 進行複習。
```

---

## 一次生成六張：Stitch 總 Prompt

線稿確認後，請將下面整段一次貼入 Stitch。不要分頁貼，也不要逐張重新設定風格：

```text
Create a complete, coherent mobile app project with exactly six separate high-fidelity screens for「我想說這句｜Say This」, a Traditional Chinese English-learning app for adults. Generate all six screens at once as distinct mobile screens/routes. Do not create one long scrolling webpage, a desktop dashboard, six visual variations of one screen, or extra screens.

Product goal:
Users enter a real-life Chinese sentence, choose context and tone, receive English matched to their proficiency level, understand the expression, save it, and review it later.

Shared design system for all six screens:
- Portrait mobile canvas, 390×844 px per screen.
- Traditional Chinese UI; English only for learning content and necessary level labels.
- Mature, calm, trustworthy, and encouraging for users age 18+; not childish or game-like.
- Cool off-white background #F7F8FC, deep navy text #172033, indigo primary #5B5BD6, teal accent #28B8A6.
- Noto Sans TC for Chinese and Inter for English.
- 16px rounded cards, subtle cool-gray borders, restrained soft shadows, generous whitespace.
- Solid indigo primary buttons with white text; outlined secondary buttons.
- Simple consistent outline icons. No photos, emojis, flags, mascots, 3D illustrations, confetti, streak flames, or heavy gradients.
- Minimum 44px touch targets, accessible text contrast, clear selected states using color plus border or icon.
- Main screens share a bottom navigation with outline icons and labels「首頁」「句子庫」「複習」. Screen 01 has no bottom navigation. Screen 04 uses a sticky learning action area instead of bottom navigation.
- Use the same component styles, typography scale, spacing, buttons, cards, chips, and icon family across all screens.

Generate these exactly six screens:

SCREEN 01 —「程度設定」
- Small brand lockup「我想說這句」with “Say This”.
- Heading「你的英文目前比較接近哪一種？」and supporting text「不用擔心，之後可以隨時調整。」
- Three stacked selectable level cards with radio controls:
  1.「入門」A1–A2／「能理解常見單字與簡單句子，希望先把意思說清楚。」
  2.「中階」B1–B2／「能應付日常對話，希望說得更自然、完整。」
  3.「進階」C1 以上／「能理解複雜內容，希望掌握細微語氣與精準用法。」
- Show「中階」selected with indigo border, tinted background, and selected radio.
- Sticky full-width primary button「開始使用」.
- No bottom navigation.

SCREEN 02 —「輸入首頁」
- Header heading「今天想說什麼？」and subtitle「把生活中的一句話，變成真正會用的英文。」
- Tappable level chip「中階 B1–B2」at top right.
- Large multiline input card labeled「你現在想用英文說什麼？」with sample input「我今天工作很多，可能會晚一點下班。」and a small character count.
- Context chips「日常」「工作」「旅行」「社交」with「工作」selected.
- Tone chips「自然」「正式」「禮貌」「輕鬆」with「自然」selected.
- Full-width primary button「看看英文怎麼說」.
- Bottom navigation with「首頁」active.

SCREEN 03 —「英文結果」
- Top app bar with back arrow and title「英文怎麼說」.
- Compact source card showing「我今天工作很多，可能會晚一點下班。」and chips「工作」「自然」「中階」.
- Dominant result card with teal label「推薦給你的說法」.
- Large English sentence: “I have a lot on my plate today, so I might get off work a little late.”
- Small explanation「日常工作場合自然、完整的說法。」and audio control「聽發音」.
- Segmented control「基礎版」「自然版」「精準版」with「自然版」selected.
- Primary button「查看解析」, secondary button「收藏這句」, and low-emphasis text action「重新調整條件」.
- Bottom navigation visible.
- Do not show full vocabulary or grammar explanations on this screen.

SCREEN 04 —「句子解析」
- Top app bar with back arrow and title「這句怎麼用」.
- Sentence header card with the full English sentence. Highlight “have a lot on my plate” with a soft teal background. Add audio action「聽發音」.
- Three concise learning cards:
  1.「重點片語」: “have a lot on my plate”／「手上有很多事要處理」／「比 have a lot of work 更口語自然。」
  2.「句型結構」: visually show「原因 I have...」→「結果 so I might...」.
  3.「語氣與場合」: chips「自然」「工作」「口語」and text「適合對同事或朋友說明今天可能晚下班。」
- Collapsed accordion「看看其他說法」with subtitle「比較基礎版與精準版」.
- Sticky bottom action area with primary button「開始練習」and secondary bookmark action「收藏這句」.
- No main bottom navigation on this screen. Keep paragraphs short.

SCREEN 05 —「我的句子庫」
- Header title「我的句子庫」and count「12 句」.
- Search field「搜尋中文或英文」.
- Scrollable filter chips「全部」「待複習」「學習中」「已熟悉」with「全部」selected, plus separate filter button「情境」.
- Show three saved sentence cards. Each includes Chinese source, English expression limited to two lines, chips such as「工作」「自然」, familiarity status, next review text such as「今天複習」or「3 天後」, audio icon, and overflow menu.
- Use text plus accessible color for status; no tables or crowded metadata.
- Bottom navigation with「句子庫」active.

SCREEN 06 —「句子複習」
- Top row with close icon, centered title「今日複習」, and progress「2／5」. Add a thin 40% progress bar.
- Main prompt card with chips「工作」「自然」, label「請試著用英文說：」and large Chinese sentence「我今天工作很多，可能會晚一點下班。」
- Large multiline answer field「輸入你的英文句子」and optional action「給我一個提示」.
- Full-width primary button「送出答案」.
- Default state is unanswered: do not reveal the correct answer. Show only a subtle collapsed note「送出後會顯示答案與解析」.
- Bottom navigation with「複習」active.
- Define later feedback states in the component styling: correct uses teal with「答對了」; incorrect uses warm amber, not red, with「再練一次就會更熟」. After submission, the design should support showing the correct answer, meaningful differences, and self-rating buttons「還不熟」「有點熟」「已熟悉」.

Create a visually consistent connected flow between the six screens:
01 開始使用 → 02 首頁
02 看看英文怎麼說 → 03 英文結果
03 查看解析 → 04 句子解析
03 收藏這句 → 05 句子庫
05 開始複習 → 06 句子複習

Label all six generated screens clearly in the project and preserve exact Traditional Chinese copy. Prioritize clarity, learning hierarchy, and realistic mobile spacing over decorative visuals.
```

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

## 老師要求的實際操作順序

1. 複製「一次生成六張：線稿總 Prompt」，一次取得六張 wireframe。
2. 檢查六張是否都有產生、流程是否完整、首頁與結果頁層級是否清楚。
3. 將「一次生成六張：Stitch 總 Prompt」整段貼入 Stitch，一次建立六個畫面。
4. 如果只有其中一頁不理想，再使用後面的單頁 Prompt 修正該頁，不要重新生成整套。
