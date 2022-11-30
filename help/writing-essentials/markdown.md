---
title: 如何使用 Markdown 語言撰寫文件
description: 了解Markdown製作的基本知識。 尋找撰寫文章所使用之Markdown語言的參考資訊。
exl-id: 3e5726e2-139e-4e44-ae5b-8a3ae4782faf
source-git-commit: e9cd46132a673d5acd1e3db2f05a9c3c8e5bc30b
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 98%

---

# 如何使用 Markdown 語言撰寫技術文件

Adobe 技術文件中的文章是以名為 [Markdown](https://daringfireball.net/projects/markdown/) 的精簡化標記語言寫成，這種語言容易閱讀及學習。

我們目前是將 Adobe 文件內容儲存在 GitHub，而 GitHub 使用的 Markdown 版本稱為 [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/)，可提供額外功能滿足常見的格式需求。 此外，Adobe 更適度擴充 Markdown 效能，以支援註釋、提示和內嵌影片等特定的說明相關功能。

## Markdown 基本介紹

以下各節將說明Markdown的製作基本概念。

### 標題

若要建立標題，請在文字行的開頭使用井字號 (#)：

```
# This is level 1 (article title)
## This is level 2
### This is level 3
#### This is level 4
##### This is level 5
```

### 基本文字

使用 Markdown 時，標示段落並不需要特殊語法。

若要將文字的格式設為&#x200B;**粗體**，請以雙星號括住文字。 若要將文字的格式設為&#x200B;*斜體*，請以單星號括住文字：

```markdown
   This text is **bold**.
   This text is *italic*.
   This text is both ***bold and italic***.
```

若要略過 Markdown 格式字元，請在該字元前使用「\」：

```markdown
This is not \*italicized\* type.
```

### 編號清單與項目符號清單

若要建立項目符號清單，請在文字行的開頭使用 `1.` 或 `1)`，但同一份清單內請勿混用不同格式。 您不必指定編號， GitHub 會自動完成編號工作。

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

顯示結果：

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

若要建立項目符號清單，請在文字行的開頭使用「\*」、「-」或「+」，但同一份清單內請勿混用不同格式。 (請勿在同一份文件中混用項目符號格式，例如 \* 和 \+)。

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

顯示結果：

* First item in an unordered list.
* Another item.
* Here we go again.

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

顯示結果：

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

### 表格

表格並非 Markdown 核心規格的一部分，但 Adobe 可在某些情況下支援表格。 Markdown 的儲存格不支援多行清單。 避免在表格中輸入多行文字，會是最理想的作法。 您可以使用直立線 (|) 字元勾勒出行、列，藉此建立表格。 連字號會建立各欄標題，直立線符號則能分隔各欄。 在表格前面加上一個空白行，以確保表格成功呈現。

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

顯示結果：

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Markdown 要呈現簡單的表格沒有問題。 不過，若表格的儲存格內包含多個段落或清單，就會難以呈現。 如果是這類內容，建議您使用其他格式，例如改為標題與文字。

如需建立表格的詳細資訊，請參閱：

* GitHub 的[使用表格組織資訊](https://help.github.com/articles/organizing-information-with-tables/)
* [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) 網頁應用程式
* [將 HTML 表格轉換為 Markdown](https://jmalarcon.github.io/markdowntables/)

### 連結

內嵌連結使用的 Markdown 語法是由超連結文字的 `[link text]` 部分，以及緊接在後的連結網址或檔案名稱 `(file-name.md)` 部分所組成。

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

顯示結果：

[Adobe](https://www.adobe.com/tw/)

若連結的是同一存放庫內的文章 (交叉參照)，請使用相對連結。 您可使用所有相對連結運算元，例如「/」(目前目錄)、「../」(上一層目錄) 和「../../」(上兩層目錄)。

```markdown
See [Overview example article](../../overview.md)
```

如需連結的詳細資訊，請參閱本指南中的[連結](linking.md)一文，瞭解連結語法。

### 影像

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

顯示結果：

![Adobe 標誌](assets/no-localize/adobe_standard_logo.png "暫留文字")

**注意：** 若有不應本地化的影像，請在資產檔案夾中另外建立一個 `do-not-localize` 檔案夾。 通常，沒有文字的影像或只包含樣本內容的影像將會放在該處。 這樣做會移除資產檔案夾中的任何「雜訊」，並減少問題的數量。

### 程式碼片段

Markdown 支援將程式碼片段內嵌在句子中，或以「包圍型」獨立片段形式插入句子之間。 如需詳細資訊，請參閱 [Markdown 對程式碼片段的原生支援](https://daringfireball.net/projects/markdown/syntax#precode)

使用反引號 (`` ` ``) 在段落中建立內嵌程式碼樣式。若要建立特定的多行程式碼區塊，請在程式碼區塊前後加上三個反引號 (` ``` `) (在 Markdown 中稱為「包圍型程式碼區塊」，在 AEM 中只是一個「程式碼區塊」元件)。若要使用包圍型程式碼區塊，請在第一組反引號之後加上程式碼語言，讓 Markdown 可以正確地標示程式碼語法。範例：` ```javascript`

範例：

```markdown
This is `inline code` within a paragraph of text.
```

顯示結果：

This is `inline code` within a paragraph of text.

這是包圍型程式碼片段：

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

## 自訂 Markdown 擴充功能

Adobe 文章中大部分的文章格式都會使用標準 Markdown，例如段落、連結、清單與標題。 若需要更豐富的格式變化，可在文章中使用 Markdown 擴充功能，例如：

* 註釋區塊
* 內嵌影片
* 不要本地化
* 元件屬性，例如為標題指定不同標題 ID

在每一行的開頭使用 Markdown 區塊引號 (「>」)，繫結擴充元件 (例如註釋)。若需在元件內使用子元件，請為該子元件區段另外新增一層區塊引號 (「>  >」)。 例如，「不要本地化」區段內的「註釋」區段應以「>    >」開頭。

部分常見的 Markdown 元素 (例如標題和程式碼區塊) 會包含擴充屬性。 如需變更預設屬性，請在元件之後新增參數，並置於大括弧內 (「/{ /}」)。 擴充屬性會以實例說明。

### 註釋區塊

您可以選擇使用這些註釋類型，以吸引讀者注意特定內容：

* `[!NOTE]`
* `[!TIP]`
* `[!IMPORTANT]`
* `[!CAUTION]`
* `[!WARNING]`
* `[!ADMINISTRATION]`
* `[!AVAILABILITY]`
* `[!PREREQUISITES]`

一般來說，註釋區塊應節制使用，註釋太多可能會造成干擾。 雖然註釋區塊也支援程式碼片段、影像、清單和連結，但請試著讓註釋區塊簡單明瞭。


```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

顯示結果：

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

顯示結果：

>[!TIP]
>
>This is a standard tip.

### 影片

原生 Markdown 不會轉譯內嵌影片，但您可以使用此 Markdown 擴充功能達成此目的。

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

顯示結果：

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### 類似項目

AEM 中的「類似項目」元件會出現在文章結尾處。 這會顯示相關連結。 文章輸出時，可採用相同的第 2 層標題 (##) 格式，不必加入迷你目錄。

```markdown
>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

顯示結果：

>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/tw/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/tw/support/audience-manager.html)


### UICONTROL 和 DNL

我們所有 Markdown 說明內容一開始會使用機器翻譯工具來進行本地化。 如果說明內容從未進行過本地化，那麼我們將保留機器翻譯。 但是，如果說明內容過去已經進行過本地化，那麼機器翻譯的內容將充當預留位置，而內容部分則在進行人工翻譯中。

**``**

在進行機器翻譯期間，系統會勾選標示為 `` 的項目，並根據本地化資料庫來決定適當的翻譯。 若 UI 當未經過本地化，此標記將允許系統保留該特定語言的英文 UI 參照 (即 義大利文的 Analytics 參照)。

**範例：**

1. 前往 **[!UICONTROL Run Process]** 畫面。
1. 選擇 **[!UICONTROL File > Print > Print All]** 以列您伺服器上的所有檔案。
1. 隨即顯示「[!UICONTROL Processing Rules]」對話框。

**來源：**

```markdown
1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.
```

**注意：** 在三個標記選項中，這是提高品質內容最重要的一項，且屬於強制規定。

**`[!DNL]`**

我們使用「不要翻譯」列表來設定規則，讓機器翻譯引擎知道哪些應該保留英文內容。 最常見的項目為解決方案的完整名稱，如「Adobe Analytics」、「Adobe Campaign」和「Adobe Target」。 但是，可能有我們需要強制引擎使用英文的情況，因為所考慮的名詞可能是用作特定專業用語或是一般用語。 最明顯的情況為解決方案的簡短名稱，如「Analytics」、「Campaign」和「Target」等。 機器很難理解這些是解決方案名稱而不是通用名詞。 該標記也可以用作一定要保留為英文或文字較短部分的第三方名稱/特性，例如必須保留為英文的短語或句子。

**範例：**

* 使用 [!DNL Target] 可建立 A/B 測試以找出最佳用法
* Adobe Analytics 是收集您網站上分析資料的強大解決方案。 [!DNL Analytics] 還可以幫助您製作報告以輕鬆地摘要資料。

**來源：**

```markdown
* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.
```

## Gotcha 與疑難排解

### 替代文字

包含底線的替代文字無法正確轉譯。 舉例來說，請避免使用下列文字：

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

在檔名中使用連字號 (「-」) 而非底線 (「_」)，會是最理想的作法。

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### 單引號與雙引號

您將文字複製到 Markdown 編輯器時，這些文字可能會含有「聰明」(彎曲) 的單引號或雙引號。 這些引號需要編碼或變更為基本的單引號或雙引號。 否則檔案發佈後，畫面可能會出現奇怪的字元，像是：Itâ€™s

在此提供這些標點符號的「聰明版」編碼：

* 左雙引號： `&#8220;`
* 右雙引號：`&#8221;`
* 右單引號：`&#8217;`
* 左單引號 (不常使用)：`&#8216;`

### 角括弧

若要在檔案中的文字 (而非程式碼) 使用角括弧 (像是要表示預留位置)，請手動編碼角括弧。 否則，Markdown 會認為這些角括弧代表 HTML 標籤。

舉例來說，請將 `<script name>` 編碼如下 `&lt;script name&gt;`

### 標題中的 &amp; 符號

不可在標題中使用 &amp; 符號。 請改用「與」或「和」，或使用 `&amp;` 編碼。

## 另請參閱

### Markdown 資源

* [Markdown 簡介](https://daringfireball.net/projects/markdown/syntax)
* [GitHub 提供的 Markdown 基本介紹](https://help.github.com/articles/markdown-basics/)
