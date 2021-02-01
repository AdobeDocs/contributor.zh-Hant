---
lastModified: 2018-06-28T00:00:00Z
title: 在文件中使用連結
seo-title: 在 Adobe Git/Markdown 文件中使用連結
description: 本文提供建立內容與影像連結的相關指示。
seo-description: 本文提供在 Adobe 文件中建立內容與影像連結的相關指示。
translation-type: tm+mt
source-git-commit: df6c4152df0c1ee87c9fc4ca22e36a3f13cb620b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 在文件中使用連結

本文說明文件頁面中超連結的使用方式。使用幾種不同作法，即可在 Markdown 內容中輕鬆新增連結。連結可將使用者引導至同一頁面中的內容、相鄰頁面或外部網站與網址。

>[!IMPORTANT]
>只要目標支援 (大多數目標都會支援)，在理想的情況下，所有連結應以安全連結的形式呈現 (`https` 和 `http` 的區別)。

## 網址連結

連結文字所含字詞應該是連結頁面的標題，或是確切的說明文字。

**範例:**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## 文章之間的連結

若要建立同一存放庫內不同文章間的內嵌連結，請使用下列連結語法:

- 從目錄中某篇文章連結至同一目錄的另一篇文章:

   `[link text](article-name.md)`

- 子目錄中某篇文章連結至根目錄的文章:

   `[link text](../article-name.md)`

- 次子目錄中某篇文章連結至根目錄的文章:

   `[link text](../../article-name.md)`

- 根目錄中某篇文章連結至子目錄的文章:

   `[link text](./directory/article-name.md)`

- 子目錄中某篇文章連結至另一個子目錄的文章:

   `[link text](../directory/article-name.md)`

- 次子目錄中某篇文章連結至另一個子目錄的文章:

   `[link text](../../directory/article-name.md)`

## 錨點連結

您不必自行建立錨點。所有 H2 標題發佈時，都會自動建立錨點。您只需建立連結至 H2 (##) 區段的連結。

- 連結同一篇文章中的標題:

   `[link](#the-text-of-the-level2-section-separated-by-hyphens)`

   `[Link to anchors](#links-to-anchors)`

- 連結同一子目錄中另一篇文章的錨點:

   `[link text](article-name.md#anchor-name)`

   `[Configure your profile](overview.md#getting-started)`

- 連結另一個服務子目錄中的錨點:

   `[link text](../directory/article-name.md#anchor-name)`

   `[Configure your profile](../overview.md#configure-your-profile)`

## 影像連結

將影像和檔案存放於要連結之 Markdown 檔案所在階層的 `assets` 目錄，會是最理想的作法。

- 文章連結至 `assets` 子目錄中的影像:

   `![alt text](assets/image-name.png)`

- 文章連結至 `assets/no-localize` 子目錄中的影像:

   `![alt text](assets/no-localize/image-name.png)`
