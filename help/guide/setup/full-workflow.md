---
title: 適用於重大變更的 GitHub 貢獻工作流程
description: 了解如何為 Experience League 上的 Adobe 文件做出貢獻。
exl-id: ad467ad4-abd2-4166-8659-e29c48d268ec
source-git-commit: a1466cb4bcbef51689c659e25d56d5cb0d4843a6
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 96%
---
# 重大變更的 GitHub 貢獻工作流程

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/tw/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
-->

## 概觀

此工作流程適合需執行重大變更或經常對存放庫做出貢獻的貢獻者。 經常貢獻者通常會長期持續執行變更作業，這些變更會先經過多次建立/驗證/測試週期，或橫跨多天時間，提取請求才能獲得簽核和合併。

### 術語

開始之前，請先檢視此工作流程所使用的 Git/GitHub 術語。

| 名稱 | 說明 |
|-----------|-------------|
| 分叉 | 通常以名詞形式使用，意指主要 GitHub 存放庫的複本。 實際上，分叉就是另一個存放庫。 然而，GitHub 之所以特別，在於其與主要/父存放庫維持雙向連線。 分叉有時會轉化為動詞概念，例如「您必須先取用並複製存放庫」。 |
| 遠端 | 與遠端存放庫之間已命名的連線，例如「來源」或「上游」遠端。 這些連線就稱為遠端，因為 Git 可藉此參考其他電腦上託管的存放庫。 在此工作流程中，遠端一律為 GitHub 存放庫。 |
| 來源 | 指派給您本機存放庫與複製來源存放庫間的連線名稱。 在此工作流程中，來源代表與存放庫複本之間的連線。 來源有時會是來源存放庫本身的別稱，例如「記得將變更推送至來源」。 |
| 上游 | 如同來源遠端，上游是與其他存放庫之間已命名的連線。 在此工作流程中，上游代表您本機存放庫與建立您存放庫複本來源的主要存放庫間的連線。 上游有時會是上游存放庫本身的別稱，例如「記得從上游提取變更」。 |

若您不熟悉 Git 和 GitHub 概念 (例如存放庫或分支)，請先參閱 [Git 和 GitHub 基本介紹](git-fundamentals.md)。

## 工作流程

>[!IMPORTANT]
>
> 請先完成[「設定」](github-signup.md)區段所述步驟。

在此工作流程中，變更會以週期重複的方式進行。 從裝置的本機存放庫開始，變更會回到 GitHub 複本、進入主要 GitHub 存放庫，並在您納入其他貢獻者提出的變更時再次回到本機。

### 使用 GitHub 流程

回想一下 [Git 和 GitHub 基本介紹](git-fundamentals.md)，Git 存放庫包含主要分支，以及其他任何尚未整合至主要分支的進行中分支。 每當您導入一組邏輯縝密的變更時，最佳作法是建立&#x200B;*工作分支*，透過工作流程管理您的變更。 我們稱之為工作分支，因為在變更可以整合回主要分支之前，它都是可反覆修訂/調整變更的工作區。

將相關變更隔離到特定分支，可讓您獨立控制並導入這些變更，將其安排在發佈週期中的特定發佈時間。 實際上，存放庫隨便都會有數個工作分支，端視您的工作類型而定。 同時在多個分支上作業並不少見，而每個分支都代表不同的專案。

<!--
>[!NOTE]
>
>Making your changes in the main branch *is not a good practice*. Imagine that you use the main branch to introduce a set of changes for a timed feature release. You finish the changes and are waiting to release them. Then in the interim, you have an urgent request to fix something, so you make the change to a file in the main branch and then publish the change. In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.
-->

接下來，您需要在本機存放庫中建立新的工作分支，以納入您提出的變更。 每個 Git 用戶端不盡相同，因此請向您偏好的用戶端服務商尋求協助。 如需程序概觀，請查閱 [GitHub 流程](https://guides.github.com/introduction/flow/)的 GitHub 指南。

## 提取請求處理

您可將提出的變更合併成新的提取請求 (PR)，新增至目的地存放庫 PR 佇列，再提交變更。 只要提取工作分支的變更並合併至其他分支，提取請求即可啟用 GitHub 的協作模型。 大多數情況下，所謂其他分支其實就是主要存放庫中的預設/主要分支。

### 驗證

提取請求可合併至目的地分支之前，可能需先完成一或多個 PR 驗證程序。 驗證程序可能會因所提出的變更範圍及目的地存放庫的規則而有所不同。 提交提取請求後，內容會經過審核，並在適當時合併至主要存放庫。

### 審核和簽核

所有PR處理作業完成後，您應先檢閱結果（PR註釋、預覽URL等）， 以確定是否需要對其檔案進行其他變更，然後再簽核以進行合併。 PR 審核者審核完您的提取要求後，若在合併前仍有未解決的問題/疑問，他們也可以透過注釋提供意見。

提取請求沒有任何問題且完成簽核後，您的變更就會合併回父分支，提取請求也會關閉。

### 發行

記住，您的提取請求必須先經由 PR 審核者合併，變更才會納入下次已排程的發佈作業。 提取請求通常會依照提交順序來審核/合併。 若您的提取請求需提前合併，以趕上特定的發佈作業，請事先與 PR 審核者商量，確保能在發佈前完成合併。
