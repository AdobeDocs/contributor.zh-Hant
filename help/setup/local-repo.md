---
title: 在本機設定 Git 存放庫
description: 本文提供建立本機 Git 存放庫和參與 Adobe 文件編撰的相關指示，包括分叉處理與複製流程。
exl-id: 679c07a2-030b-4a30-ba14-7780f88dae11
source-git-commit: a3c283c5c0d181beacc566262743528d5ff9f7d2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 98%

---

# 在本機設定供文件使用的 Git 存放庫

本文以參與 Adobe 文件編寫為目的，說明在本機電腦上設定 Git 存放庫的步驟。貢獻者可使用複製到本機的存放庫來新增文章、對現有文章做出重大編輯或變更插圖。

>[!IMPORTANT]
>若您僅需微幅修改文章，*不需要*&#x200B;完成本文所述步驟。只要在瀏覽器中按一下編輯圖示，即可編輯文字。

## 概述

若要參與 Adobe 文件編寫，您可以取用合適的存放庫並將其複製到自己的 GitHub 帳戶，如此便能擁有讀取/編寫權限。接著，複製對應的文件存放庫，就能在本機建立及編輯 Markdown 檔案。接下來，您可使用提取請求，將變更合併 (提交) 至唯讀的集中式共用存放庫。

* 確定合適的存放庫
* 取用存放庫並複製到您的 GitHub 帳戶
* 選擇本機資料夾以存放複製的檔案
* 將存放庫複製到本機電腦
* 設定上游遠端的值

## 確定存放庫

取用合適的存放庫並複製到您自己的 GitHub 帳戶，這樣您就擁有讀取/編寫權限，可儲存您要做的變更。[!UICONTROL Adobe Experience Cloud]檔案位於[github.com](https://www.github.com/adobedocs)的多個不同的存放庫。

1. 若不確定要使用哪個存放庫，可使用網頁瀏覽器查看文章。選取文章右上角的&#x200B;**編輯**&#x200B;連結 (鉛筆圖示) (如果沒有顯示編輯連結，表示還無法在 GitHub 使用該內容)。

若要對 Adobe 文件做出貢獻，請複製對應的文件存放庫，這樣就能在本機上建立及編輯 Markdown 檔案。接下來，您可使用提取請求，將變更合併至唯讀的集中式共用存放庫。

<!---
![GitHub Triangle](/assets/git-and-github-initial-setup.png)

If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]
-->

## 建立存放庫複本

找到合適的存放庫後，請使用 GitHub 網站，在您自己的 GitHub 帳戶中建立存放庫複本。

由於所有主要文件存放庫僅提供唯讀權限，表示您不能直接在存放庫中修改內容，因此需要自行建立複本。若要變更內容，您必須向主要存放庫提交複本提取請求 (PR)。為方便此流程進行，首先需建立一個您可以擁有編寫權限的存放庫複本。GitHub *取用*&#x200B;功能即為此目的而生。

1. 前往主要存放庫的 GitHub 頁面，然後按一下右上角的 **Fork** (分叉) 按鈕。

   ![GitHub 分叉功能](assets/fork-simple.png)

1. 一旦系統顯示提示，請選取您的 GitHub 帳戶，作為建立複本的目的地。此提示會在您的 GitHub 帳戶中建立存放庫複本 (即所謂的分叉)。

1. 選擇方便記憶與輸入的資料夾名稱。

   有些存放庫可能規模龐大。請選擇磁碟空間充足的儲存位置。

   >[!NOTE]
   >
   >避免選擇其他 Git 存放庫資料夾位置下的巢狀本機資料夾路徑。雖然 Git 複製資料夾可以並列存放，巢狀的 Git 資料夾會造成檔案追蹤上的錯誤。

## 在本機建立存放庫複本

複製您要使用的存放庫，會將檔案的複本下載到您的電腦上。準備就緒後，您可從本機磁碟將編輯項目推送到伺服器上您所取用的存放庫。接著，您可以提交提取請求，將編輯項目合併到上游的主存放庫。

這些步驟只適用於 GitHub Desktop。若是使用其他用戶端，請適度調整作法。

1. 按一下 **Clone or download** (複製或下載)，然後選擇 **Open in Desktop** (在 Desktop 中開啟)，將存放庫複本 (亦即您建立的分叉) 提取到您電腦的目錄。

   ![複製存放庫](assets/clone-pulldown.png)

1. 使用 GitHub Desktop 可保持本機檔案與取用的存放庫保持同步。

詳情請參閱 [GitHub Desktop 文件](https://help.github.com/desktop/)。
