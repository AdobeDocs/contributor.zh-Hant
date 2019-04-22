---
lastModified: 2018/06/28
title: 如何使用 Markdown 語言撰寫文件
seo-title: 如何使用 Markdown 語言撰寫 Adobe 文件
description: 本文提供撰寫文章時所需的 Markdown 語言基本概念與參考資訊。
seo-description: 本文提供撰寫 Adobe 文件時所需的 Markdown 語言基本概念與參考資訊。
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---

# 如何使用 Markdown 語言撰寫技術文件

Adobe 技術文件中的文章是以名為 [Markdown](https://daringfireball.net/projects/markdown/) 的精簡化標記語言寫成，這種語言容易閱讀及學習。

我們目前是將 Adobe 文件內容儲存在 GitHub，而 GitHub 使用的 Markdown 版本稱為 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/)，可提供額外功能滿足常見的格式需求。此外，Adobe 更適度擴充 Markdown 效能，以支援註釋、提示和內嵌影片等特定的說明相關功能。

## Markdown 基本介紹

### 標題

若要建立標題，請在文字行的開頭使用井字號 (#):

```
   # This is level 1 (article title)
   ## This is level 2
   ### This is level 3
   #### This is level 4
   ##### This is level 5
```

### 基本文字

使用 Markdown 時，標示段落並不需要特殊語法。

若要將文字的格式設為**粗體**，請以雙星號括住文字。若要將文字的格式設為*斜體*，請以單星號括住文字:

```markdown
    This text is **bold**.
    This text is *italic*.
    This text is both ***bold and italic***.
```

<!--
To format superscript (H<sub>2</sub>O) and subscript (e=mc<sup>2</sup>) text:

```markdown
This is subscript H<sub>2</sub>O and superscript e=mc<sup>2</sup>.
```
-->

若要略過 Markdown 格式字元，請在該字元前使用「\」:

```markdown
This is not \*italicized\* type.
```

### 編號清單與項目符號清單

若要建立編號清單，請在文字行的開頭使用「1」或「1)」，但同一份清單內請勿混用兩種格式，否則會額外建立另一份清單。您不必指定編號，GitHub 會自動完成編號工作。

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

顯示結果:

1. 這是第 1 步。
1. 這是下一步。
1. 還有第 3 步。

<!-- markdownlint-disable MD037 -->
若要建立項目符號清單，請在文字行的開頭使用「\*」、「-」或「+」，但同一份清單內請勿混用不同格式(若混用格式，例如同時使用「\*」和「\+」，系統會額外建立另一份清單)。
<!-- markdownlint-disable MD037 -->

```markdown
- First item in an unordered list.
- Another item.
- Here we go again.
```

顯示結果:

- 未排序清單的第一個項目。
- 另一個項目。
- 再來一個項目。

清單內也可以內嵌清單，並在清單項目間新增內容。

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this: 

    | Hello | World |
    |---|---|
    | How | are you? |  
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
1. Do another step.
```

顯示結果:

1. 設定表格與程式碼片段。
1. 執行此步驟。

   ![畫面](assets/no-localize/adobe_standard_logo.png)
1. 確定表格看起來像這樣:

   | Hello | World |
   |---|---|
   | How | are you? |
1. 這是第四步。

   >[!NOTE]
   >
   >這是註釋文字。
1. 再來一個步驟。

### 表格

表格並非 Markdown 核心規格的一部分，但 Adobe 可在某些情況下支援表格。Markdown 的儲存格不支援多行清單。避免在表格中輸入多行文字，會是最理想的作法。您可以使用直立線 (|) 字元勾勒出行、列，藉此建立表格。連字號會建立各欄標題，直立線符號則能分隔各欄。在表格前面加上一個空白行，以確保表格成功呈現。

```markdown
| Header | Another header | Yet another header |
|------------|:---------------:|-----------------------:|
| row 1 | centered column 2 | right-aligned column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

顯示結果:

| 標題 | 另一個標題 | 再一個標題 |
|------------|:---------------:|-----------------------:|
| 第 1 列 | 第 2 欄置中對齊 | 第 3 欄靠右對齊 |
| 第 2 列 | 第 2 列第 2 欄 | 第 2 列第 3 欄 |

Markdown 要呈現簡單的表格沒有問題。不過，若表格的儲存格內包含多個段落或清單，就會難以呈現。如果是這類內容，建議您使用其他格式，例如改為標題與文字。

如需建立表格的詳細資訊，請參閱:

- GitHub 的[使用表格組織資訊](https://help.github.com/articles/organizing-information-with-tables/)
- [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) 網頁應用程式
- [將 HTML 表格轉換為 Markdown](https://jmalarcon.github.io/markdowntables/)

### 連結

內嵌連結使用的 Markdown 語法是由超連結文字的 `[link text]` 部分，以及緊接在後的連結網址或檔案名稱 `(file-name.md)` 部分所組成。

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com) or <https://www.adobe.com>
```

顯示結果:

[Adobe](https://www.adobe.com) 或 <https://www.adobe.com>

若連結的是同一存放庫內的文章 (交叉參照)，請使用相對連結。您可使用所有相對連結運算元，例如「/」(目前目錄)、「../」(上一層目錄) 和「../../」(上兩層目錄)。

```markdown
See [Overview example article](../../overview.md)
```

如需連結的詳細資訊，請參閱本指南中的[連結](linking.md)一文，瞭解連結語法。

### 影像

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

顯示結果:

![Adobe 標誌](assets/no-localize/adobe_standard_logo.png "暫留文字")

### 程式碼片段

Markdown 支援將程式碼片段內嵌在句子中，或以「包圍型」獨立片段形式插入句子之間。如需詳細資訊，請參閱 [Markdown 對程式碼片段的原生支援](https://daringfireball.net/projects/markdown/syntax#precode)

使用反引號 (「\`」)，在段落中建立內嵌程式碼樣式。若要建立特定的多行程式碼片段，在程式碼區塊前後新增三個反引號 (「\`\`\`」) (Markdown 稱之為「包圍型程式碼片段」，但在 AEM 中，這只是「程式碼片段」元件)。若要使用包圍型程式碼片段，請在第一組反引號之後加上程式碼語言名稱，讓 Markdown 可以正確地標示程式碼語法。範例: \`\`\`javascript

範例:

```markdown
This is `inline code` within a paragraph of text.
```

顯示結果:

這是文字段落中間的 `inline code`。

這是包圍型程式碼片段:

```markdown
\```javascript
function test() {
 console.log("notice the blank line before this function?");
\```
```

顯示結果:

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

您可以指定程式碼片段的屬性，以關閉行號 (預設為開啟) 或新增自動換行 (預設為關閉)。請使用 {line-numbers=”no”} 和 {line-wrap=”yes”} 來指定。這些屬性都是可自訂的 Markdown 擴充功能。

\`\`\`javascript {line-numbers=”no”}
function test() {
console.log(”注意到此函式前的空白行了嗎?");
\`\`\`

### 定義清單

定義清單是 Markdown 的擴充功能，可支援 AEM 的定義清單元件。定義清單包含詞彙和定義。

<!--

```markdown
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

Displayed:

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
--->

#### 備註與註解

公開的說明文章中不會顯示註解 (備註)。不過，若是使用者可以查看與編輯的公開 Markdown 檔案，就會顯示註解。

## 自訂 Markdown 擴充功能

Adobe 文章中大部分的文章格式都會使用標準 Markdown，例如段落、連結、清單與標題。若需要更豐富的格式變化，可在文章中使用 Markdown 擴充功能，例如:

- 註釋區塊
- 內嵌影片
- 不要本地化
- 元件屬性，例如為標題指定不同標題 ID

在每一行的開頭使用 Markdown 區塊引號 (「>」)，繫結擴充元件 (例如註釋)。若需在元件內使用子元件，請為該子元件區段另外新增一層區塊引號 (「>  >」)。例如，「不要本地化」區段內的「註釋」區段應以「>    >」開頭。

部分常見的 Markdown 元素 (例如標題和程式碼區塊) 會包含擴充屬性。如需變更預設屬性，請在元件之後新增參數，並置於大括弧內 (「/{ /}」)。擴充屬性會以實例說明。

### 註釋區塊

您可選擇使用四種註釋類型，以吸引讀者注意特定內容:

- `[!NOTE]`
- `[!CAUTION]`
- `[!TIP]`
- `[!IMPORTANT]`

一般來說，註釋區塊應節制使用，註釋太多可能會造成干擾。雖然註釋區塊也支援程式碼片段、影像、清單和連結，但請試著讓註釋區塊簡單明瞭。


```markdown
>[!NOTE]
>This is a standard NOTE block.
```

顯示結果:

>[!NOTE]
>這是標準的「註釋」區塊。

```markdown
>[!TIP]
>This is a standard tip.
```

顯示結果:

>[!TIP]
>這是標準的提示。

### 影片

原生 Markdown 不會轉譯內嵌影片，但您可以使用此 Markdown 擴充功能達成此目的。

```markdown
>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)
```

顯示結果:

>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)

### 類似項目

AEM 中的「類似項目」元件會出現在文章結尾處。這會顯示相關連結。文章輸出時，可採用相同的第 2 層標題 (##) 格式，不必加入迷你目錄。

<!--
```markdown
>[!MORE]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html){target="new-window"}
```

Displayed:

>[!MORE]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html){target="new-window"}
-->

### DNL - 不要本地化 - 以及 UICONTROL

某些情況下，我們需要標示文章中特定區段的內容，使這些區段保留為英文。您需要向翻譯系統宣告字詞、詞句和其他元素，並建立管理受控語彙的功能。

若字詞或詞句不應本地化，請使用 `[!DNL]` 擴充功能包住字詞或區段。

若是使用者介面中的元素或解決方案選單，則請使用 `[!UICONTROL]` 擴充功能。

**範例:**

In [!DNL Adobe Target] you can create your tests directly on a [!DNL Target]-enabled page.

**來源:**

```markdown
In [!DNL Adobe Target] you can create your tests directly on a [!DNL Target]-enabled page.
```

**範例**

使用 [!UICONTROL Visual Experience Composer] in [!DNL Target] ，直接在頁面上建立測試。

**來源:**

```markdown
Use the [!UICONTROL Visual Experience Composer] in [!DNL Target] to create your test directly on a page.
```

## Gotcha 與疑難排解

### 替代文字

包含底線的替代文字無法正確轉譯。舉例來說，請避免使用下列文字:

```markdown
![Settings_Step_2] (/assets/settings_step_2.png)
```

在檔名中使用連字號 (「-」) 而非底線 (「_」)，會是最理想的作法。

```markdown
![Settings-Step-2] (/assets/settings-step-2.png)
```

### 單引號與雙引號

您將文字複製到 Markdown 編輯器時，這些文字可能會含有「聰明」(彎曲) 的單引號或雙引號。這些引號需要編碼或變更為基本的單引號或雙引號。否則檔案發佈後，畫面可能會出現奇怪的字元，像是: Itâ€™s

在此提供這些標點符號的「聰明版」編碼:

- 左雙引號: `&#8220;`
- 右雙引號: `&#8221;`
- 右單引號: `&#8217;`
- 左單引號 (不常使用): `&#8216;`

### 角括弧

若要在檔案中的文字 (而非程式碼) 使用角括弧 (像是要表示預留位置)，請手動編碼角括弧。否則，Markdown 會認為這些角括弧代表 HTML 標籤。

舉例來說，請將 `<script name>` 編碼如下 `&lt;script name&gt;`

### 標題中的 & 符號

不可在標題中使用 & 符號。請改用「與」或「和」，或使用 `&amp;` 編碼。

## 另請參閱

### Markdown 資源

- [Markdown 簡介](https://daringfireball.net/projects/markdown/syntax)
- [GitHub 提供的 Markdown 基本介紹](https://help.github.com/articles/markdown-basics/)
