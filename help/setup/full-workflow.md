---
lastModified: 2018/06/28
title: 重大變更的 GitHub 貢獻工作流程
seo-title: Adobe 文件需有重大變更時的 GitHub 貢獻工作流程
description: 本文說明如何使用「重大」貢獻工作流程，對 Adobe 文件有所貢獻。
seo-description: 本文說明如何使用「重大」貢獻工作流程，對 Adobe 文件有所貢獻。
translation-type: ht
source-git-commit: cb9e20da64bb04a2b1765338b237825cae7aabeb

---


# 重大變更的 GitHub 貢獻工作流程

<!--
> [!IMPORTANT]
> All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## 概述

此工作流程適合需執行重大變更或經常對存放庫做出貢獻的貢獻者。經常貢獻者通常會長期持續執行變更作業，這些變更會先經過多次建立/驗證/測試週期，或橫跨多天時間，提取請求才能獲得簽核和合併。

### 術語

開始之前，請先檢視此工作流程所使用的 Git/GitHub 術語。

| 名稱 | 說明 |
|-----------|-------------|
| 分叉 | 通常以名詞形式使用，意指主要 GitHub 存放庫的複本。實際上，分叉就是另一個存放庫。然而，GitHub 之所以特別，在於其與主要/父存放庫維持雙向連線。分叉有時會轉化為動詞概念，例如「您必須先取用並複製存放庫」。 |
| 遠端 | 與遠端存放庫之間已命名的連線，例如「來源」或「上游」遠端。這些連線就稱為遠端，因為 Git 可藉此參考其他電腦上託管的存放庫。在此工作流程中，遠端一律為 GitHub 存放庫。 |
| 來源 | 指派給您本機存放庫與複製來源存放庫間的連線名稱。在此工作流程中，來源代表與存放庫複本之間的連線。來源有時會是來源存放庫本身的別稱，例如「記得將變更推送至來源」。 |
| 上游 | 如同來源遠端，上游是與其他存放庫之間已命名的連線。在此工作流程中，上游代表您本機存放庫與建立複本之主要存放庫間的連線。上游有時會是上游存放庫本身的別稱，例如「記得從上游提取變更」。 |

若您不熟悉 Git 和 GitHub 概念 (例如存放庫或分支)，請先參閱 [Git 和 GitHub 基本介紹](git-fundamentals.md)。

## 工作流程

>[!IMPORTANT]
> 請先完成[「設定」](github-signup.md)區段所述步驟。

在此工作流程中，變更會以週期重複的方式進行。從裝置的本機存放庫開始，變更會回到 GitHub 複本、進入主要 GitHub 存放庫，並在您納入其他貢獻者提出的變更時再次回到本機。

### 使用 GitHub 流程

回想一下 [Git 和 GitHub 基本介紹](git-fundamentals.md)，Git 存放庫包含主分支，以及其他任何尚未整合至主分支的進行中分支。每當您導入一組邏輯縝密的變更時，最佳作法是建立*工作分支*，透過工作流程管理您的變更。變更可以整合回主分支前，這都是可反覆查詢/調整變更的工作區，因此我們稱之為工作分支。

隔離對特定分支進行的相關變更，即可單獨控制並導入這些變更，將其鎖定至發佈週期中的特定發行時間。實際上，存放庫隨便都會有數個工作分支，端視您的工作類型而定。同時存在多個分支是很常見的現象，而每個分支都代表不同專案。

>[!NOTE]
>在主分支中執行變更作業*並非理想作法*。假設您使用主分支，為限時的功能版本導入一組變更項目。您順利完成變更，準備發行版本。但在過渡期間，您收到要求您修正某部分的緊急請求，因此您需要變更主分支中的檔案，接著再發佈變更。這個例子中，您不小心發佈了修正*和*保留要在特定日期發佈的變更。

接下來，您需要在本機存放庫中建立新的工作分支，擷取您提出的變更。每個 Git 用戶端不盡相同，因此請向您偏好的用戶端服務商尋求協助。如需程序概述，請查閱 [GitHub 流程](https://guides.github.com/introduction/flow/)的 GitHub 指南。

## 提取請求處理

您可將提出的變更合併成新的提取請求 (PR)，新增至目的地存放庫 PR 佇列，再提交變更。只要提取工作分支的變更並合併至其他分支，提取請求即可啟用 GitHub 的協作模型。大多數情況下，所謂其他分支其實就是主要存放庫中的預設/主分支。

### 驗證

提取請求可合併至目的地分支之前，可能需先完成一或多個 PR 驗證程序。驗證程序可能會因所提出的變更範圍及目的地存放庫的規則而有所不同。提交提取請求後，內容會經過審核，並在適當時合併至主要存放庫。

### 審核和簽核

所有 PR 處理作業完成後，您應先查看結果 (包括 PR 注釋、預覽網址)，確定檔案是否需要其他變更，而後才可簽核以供合併。PR 審核者審核完您的提取要求後，若在合併前仍有未解決的問題/疑問，他們也可以透過注釋提供意見。

提取請求沒有任何問題且完成簽核後，您的變更就會合併回父分支，提取請求也會關閉。

### 發行

記住，您的提取請求必須先經由 PR 審核者合併，變更才會納入下次已排程的發佈作業。提取請求通常會依照提交順序來審核/合併。若您的提取請求需提前合併，以趕上特定的發佈作業，請事先與 PR 審核者商量，確保能在發佈前完成合併。

貢獻內容通過核准並完成合併後，docs.microsoft.com 發佈程序就會加以取用。依管理您貢獻的存放庫團隊而定，實際的發佈時間可能會有所不同。
