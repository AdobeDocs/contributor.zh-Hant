---
title: Git 和 GitHub 文件基本資訊
seo-title: Git 和 GitHub 文件基本資訊
description: 本文概述 Git、GitHub 存放庫相關資訊，並說明內容的組織方式及 Adobe 文件的命名慣例。
seo-description: 本文概述 Git、GitHub 存放庫相關資訊，並說明內容的組織方式及 Adobe 文件的命名慣例。
translation-type: ht
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---

# Git 和 GitHub 文件基本資訊

## 概述

若文章只需微幅的純文字變更，您不需要瞭解本文的詳細資訊。本文主要說明重大編輯作業的工作流程，例如建立新文章、新增影像或持續編輯 Adobe 文件。

Adobe 文件內容的貢獻者可善用多種工具和程序。您可與同一專案中的其他貢獻者同步工作，甚至是編輯完全相同的內容。透過 Git 和 GitHub 軟體，便可實現這一切。

Git 是開放原始碼版本控制系統，可供多人協作。多位貢獻者可共同處理*存放庫*中的檔案。

GitHub 是適用於 Git 存放庫 (例如存放 [docs.adobe.com](https://docs.adobe.com) 內容的存放庫) 的網頁型託管服務。不論任何專案，GitHub 皆會託管主要存放庫，貢獻者可從中建立工作複本。

## Git

Git 擁有獨特的貢獻工作流程和術語，可支援其分散式模型。例如，沒有簽出/簽入操作一般會有的檔案鎖定機制。Git 能以更精細的程度解決變更，將檔案以逐位元組的方式相互比較。

此外，Git 也採取分層結構存放及管理專案的內容:

- *存放庫*: 英文簡稱為 *repo*，是最高的存放單位。存放庫包含一或多個分支。
- *分支*: 所有存放庫皆包含一個預設分支 (通常名為「主分支」)，以及一或多個會合併回主分支的分支。主分支是發佈內容的最新版本和來源，也是存放庫中其他所建立分支的父分支。

貢獻者可與 Git 互動，在本機和 GitHub 層級更新和控制存放庫:

- 利用工具 (例如 GitHub 桌面版) 即可在本機上操作。
- [www.github.com](https://www.github.com) 整合 Git，可管理及調整回到主要存放庫的貢獻內容。

## GitHub

所有工作流程都會在 GitHub 層級開始和結束，所有 Adobe 文件專案的主要存放庫皆儲存於此層級。貢獻者為因應自身用途所建立的複本會分佈在多部電腦上。這些複本最終會調整回專案的主要 GitHub 存放庫。

### 目錄組織

專案的預設/主分支為目前的專案內容版本。主分支中的內容 (以及從中建立的分支) 會與文章主題的組織方式一致。組織內容和影像資產時會使用子目錄。

通常可以從存放庫的根目錄中找到主要`help`目錄。文章目錄包含一系列子目錄。子目錄中的文章會格式化為使用 *.md* 副檔名的 Markdown 檔案。

在此目錄的根目錄內，您可以找到與整體服務或產品相關的一般文章。通常您可以找到其他與功能/服務或常見案例相符的子目錄。

### 資產目錄

使用者指南目錄包含目錄中所引用之影像檔案的`/assets`子目錄。

<!---
### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. It also includes SEO optimizations and reporting processes that Adobe uses to evaluate the performance of the content. So the metadata is important!
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.adobe.com extensions**, which you can use for special controls such as buttons and selectors.
-->

## 提取請求

*提取請求*是一種便利方式，可供貢獻者提出要套用至預設分支的變更。變更 (又稱為*提交項目*) 會存放於貢獻者的分支中，因此 GitHub 可以先模擬將變更*合併*至預設分支的影響。提取請求也是透過建置/驗證程序(提取請求審核者) 為貢獻者提供意見的反饋機制，以便在變更合併至預設分支前解決潛在的問題或疑問。

透過提取請求貢獻內容有兩種方式，端視您要提出的變更大小而定。稍後我們會在本指南的 [GitHub 工作流程](local-repo.md)章節中詳述。
