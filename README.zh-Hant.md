[English](README.md) | **繁體中文**

# Kefir World

Kefir World 是一個以研究證據為基礎的世界發酵乳知識庫，收錄牛奶克菲爾、中溫型發酵乳、嗜熱型優格、各地傳統發酵乳，以及乳酸菌與酵母共同發酵的產品。

## 專案目標

- 建立世界各地發酵乳產品與發酵菌種的結構化目錄。
- 比較發酵溫度、時間、微生物生態、質地、酸度、香氣與傳代特性。
- 區分菌粒型菌種、回種菌種、中溫型菌種、嗜熱型菌種，以及乳酸菌－酵母混合系統。
- 讓溫度範圍與微生物主張都可追溯至可靠文獻。
- 建立可供圖表、海報、地圖與互動網站使用的資料。

## 初步溫度分類

- 中溫型／室溫發酵：約 15–30 °C
- 中間型：約 25–37 °C
- 嗜熱型／加溫培養：約 37–45 °C

這些是便於整理資料的實用分組，並非嚴格的分類學定義。不同產品與菌株的適用溫度可能重疊。

## 收錄範圍

目錄包含最初的 34 筆資料，以及十二種有來源支援的新增產品：**Ititu、Mursik、Ayran、Doogh、Labneh Ambaris、Tarag、Ryazhenka、Varenets、Katyk、Khoormog、Pendidam 與 Kindirmou**。工業型 Laban 與 Zabadi 在資料集中各有獨立一列，但分別與傳統型共用同一份 profile，讓不同製程可以在同一頁比較。

## 儲存庫結構

- [`data/fermented_milk.csv`](data/fermented_milk.csv) — 核心產品目錄
- [`data/references.csv`](data/references.csv) — 共用參考文獻登入表
- [`data/manufacturer_processes.csv`](data/manufacturer_processes.csv) — 來源特定的商業菌種啟用、發酵與回種觀察
- [`profiles/zh-Hant/`](profiles/zh-Hant/) — 44 份繁體中文產品 profile 與索引
- [`profiles/`](profiles/) — 英文產品 profile
- [`docs/data_dictionary.zh-Hant.md`](docs/data_dictionary.zh-Hant.md) — 中文欄位定義與證據規則
- [`research/roadmap.zh-Hant.md`](research/roadmap.zh-Hant.md) — 中文研究路線圖與驗證計畫
- [`research/freshly-fermented-instructions-audit.zh-Hant.md`](research/freshly-fermented-instructions-audit.zh-Hant.md) — Freshly Fermented 操作說明庫的來源稽核與整合決策

## 詳細產品資料

每一列產品都連到詳細 profile，涵蓋產品身分與歷史、傳統與現代製作方式、使用乳種、有文獻配對支援的溫度與時間、感官特性、微生物生態、已發表的分離株或菌株程式碼、胞外多醣（EPS）、酸化、傳代、儲存與證據缺口。

[開啟 44 種產品的繁體中文索引](profiles/zh-Hant/README.md)

目前的 44 份 profile 包括：

- 北歐與歐洲：Milk Kefir、Viili、Långfil、Filmjölk、Piimä、Tettmelk、Skyr、Ryazhenka、Varenets。
- 亞洲與高加索：Caspian Sea Yogurt、Dadih、Tarag、Khoormog、Katyk、Chal/Shubat、Kumis/Airag、Matsoni、Dahi、Mishti Doi。
- 非洲：Ergo、Ititu、Dhanaan、Nunu、Mabisi、Amasi、Suusac、Mursik、Kindirmou、Pendidam、Lben、Rayeb。
- 中東：Laban、Zabadi、Ayran、Doogh、Labneh，以及製程不同且耗時較長的 Labneh Ambaris。
- 明確組成或經濃縮的發酵乳：Traditional Yogurt、Greek Yogurt、Bulgarian Yogurt、Acidophilus Milk、Bifidus Milk、AB Yogurt、ABT Yogurt。

找不到可靠的菌株程式碼、製程溫度或儲存時間時，profile 會明確標為未知。傳統型／工業型 Laban 與 Zabadi 的共用 profile 仍會分開呈現兩種製程。

## 證據原則

溫度、微生物、來源與發酵時間皆應視為需要文獻支援的資料。傳統產品會因家戶、地區、乳種與菌種系譜而有差異，因此本專案保留每個來源的實際條件，不把彼此無關的實驗合併成一個「通用配方」。

繪圖前請先閱讀 `fermentation_scope`。某些區間代表兩套不同且相互配對的製程；上下限相同則可能只表示文獻中的近似操作點。這些欄位不代表微生物的生理耐受極限。物種檢出、具名分離株、商業混合菌種與序列登入號也會分開記錄。

中文 profile 保留拉丁學名、菌株程式碼、參考文獻程式碼、DOI 與英文論文題名，方便逐項追溯。若中英文敘述有差異，以英文 profile 與引用的原始來源為核對依據。

## 目前狀態

目錄共有 **46 種產品、44 份 profile 與 149 筆可追溯參考文獻**。所有資料列均已有文獻支援狀態與明確的製程範圍；但「有文獻支援」不代表每一項特徵都已有一致結論或獨立重複驗證。

商業製程觀察另存於獨立資料表，使菌種啟用與供應商配方可以被查詢，又不會被誤認為通用傳統製法。[Freshly Fermented 稽核頁](research/freshly-fermented-instructions-audit.zh-Hant.md)記錄完整 sitemap 篩選、15 個已整合的產品頁面與未採納的主張。

2026-09-07 至 2026-09-08 的審查也修正了早期草稿中的部分假設：空白數值表示找不到可辯護的通用值；不能把「環境溫度」換算成自行推測的數字；混合菌種程式碼不是菌株；同名產品下的不同製程應分別儲存，不應平均成誤導性的區間。
