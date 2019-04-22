---
lastModified: 2018/06/28
title: 在文件中使用連結
seo-title: 在 Adobe Git/Markdown 文件中使用連結
description: 本文提供建立內容和影像連結的指引。
seo-description: 本文章提供建立Adobe文件內容與影像連結的指引。
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# 在文件中使用連結

本文說明文件頁面中的超連結使用。使用幾種不同作法，即可在 Markdown 內容中輕鬆新增連結。連結可將使用者引導至同一頁面中的內容、相鄰頁面或外部網站與網址。

> [!IMPORTANT]
> 當目標支援時，所有連結最好是安全連結(`https` 相對於 `http`)。

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

<!--
## Bob's link test

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> File Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated values file (such as one created in Excel). This is the file that contains the customer attribute data. See [Link TEST](/help/setup/full-workflow.md) </p> <p> <b>Naming requirements:</b> Ensure that file name extensions do not contain white spaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Required) The <span class="filepath"> .fin </span> file tells the system that you are finished uploading data. The name of the <span class="filepath"> .fin </span> file must match the name of the <span class="filepath"> .csv </span> file. </p> <p>Adobe recommends creating an empty text file with a <span class="filepath"> .fin </span> extension. An empty file saves space and upload time. </p> <p> <p>Note:  Renaming a <span class="filepath"> .fin </span> file is not allowed after it is uploaded. The <span class="filepath"> .fin </span> file must be uploaded separately and cannot be a renamed, previously uploaded file. </p> </p> <p>After you upload the <span class="filepath"> .fin </span> file in the customer attributes FTP, the system retrieves data quickly (within one minute). This differs from other Adobe FTP-based systems, which pick up data less frequently (around once per hour). </p> <p>The <span class="filepath"> .fin </span> file is not required when using the drag-and-drop upload method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> or <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) or <span class="filepath"> .zip </span> - for compressed files. A <span class="filepath"> .zip </span> file cannot contain more than one file in the archive. </p> <p> <b>Naming requirements:</b> The name of the <span class="filepath"> .zip </span> or <span class="filepath"> .gz </span> should match the name of the <span class="filepath"> .csv </span>. For example, if your <span class="filepath"> .csv </span> file is <span class="filepath"> crm_small.csv </span>, the <span class="filepath"> .zip </span> file should be <span class="filepath"> crm_small.csv.zip </span>. </p> <p>The .fin file must match the .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->
