# Git學習遊戲
Git學習遊戲是為了可以透過遊戲方式來學習Git，並真正的了解「分散式版本控管系統」(DVCS, Distributed Version Control System)、物件特性與內部運作方式，雖然可能會與真正的Git會有不同，但會以Git運作方式去設計，但在設計上面會以引導方式去操作，也就是比對不同的運作方式去比對，去思考這樣的好處。

課程的方向、學習的方式與操作的模式會依照以下重點規劃:
> 由簡單到困難  
> 實際流程到問題解決  
> 個人到群體  

# 章節
- 遊戲
  - 你會怎麼做？
  - 點
    - 你會如何保存？
    - 原點:init
  - 線
    - 你會如何紀錄？
    - 產點生線:add、status、commit
    - 觀點看線:log
  - 支
    - 你會如何協作？
    - 製作支:branch
    - 且換支:checkout
    - 合併支:merge
  - 進退
    - 你會如何修正錯誤？
    - 返回:reset
    - 倒退:revert
    - 你會如何站在巨人的肩膀上？
    - 摘取:cherry-pick
    - 站在巨人的肩膀:rebase
  - 雲與地
    - 你會如何備份與同步？
    - clone、remote、fetch、pull、push
  - 小技巧大功用
    - 你會需要什麼？
    - 圖釘與標籤:tag
    - 看不見:.gitgnore
    - 天在看:reflog

還在製作:
- 敏捷軟體開發、Scrum、DevOps
- Markdown
- 專案管理系統、「工作流程看板」(Boards)
- 各行各業應用討論

# 遊戲
## 你會怎麼做？
「你會怎麼做？」是為了希望大家在學習Git之前前先思考與分享你會如何管理、紀錄、協作、解決錯誤與備份，以及使用的小技巧，同時分享一下如何應用在工作，也是作為沒有玩遊戲直接簡報的時候的解決方法。

**器材**  
椅子、地墊等

**時間**:依人數分配，以30分鐘以內為主。

**人數**  
無限制

**重點**
- 分享與討論
- 每個人輪流
- 圍圈圈
- 統計使用方式的人數

**流程**
1. 大家圍圈
2. 依序分享你是如何解決以下問題:
  - 你會如何保存？
  - 你會如何紀錄？
  - 你會如何協作？
  - 你會如何修正錯誤？
  - 你會如何備份與同步？
  - 你會需要什麼？
3. 以迴紋針、文件、掃描列印機與資料夾來示範你的方法
4. 如何應用在工作上

## 點
### 你會如何保存？
「你會如何保存？」其重點是討論與分享如何管理檔案，以及學習如何模擬編輯純文字文件，目的是為了後續的活動中可以使用，這裡會以迴紋針、紙、資料夾與資料櫃等來讓大家實際實作與討論。

**器材**  
- 很多大迴紋針
- 很多A4紙張
- 鉛筆、原子筆或者麥克筆
- 資料夾:L夾等可以裝文件的東西
- 資料櫃:可以裝很多資料夾的櫃子，沒有櫃子可以用資料夾

**時間**:依人數分配，以一小時為主。

**人數**  
無限制

**重點**
- 分享與討論
- 使用迴紋針模擬文字

**流程**
1. 每個人發一小袋迴紋針、數十張紙、三個資料夾
2. 將A4紙張依照說明折
3. 將迴紋針插入在對折處
4. 將他放入到資料夾內
5. 放入到櫃子，如果沒有櫃子沒關係，可以同一張桌子疊在一起
6. 問大家如果你要備份，你會怎麼用？
    1. 每一個備份一次，直接在資料夾所在位置
    2. 將目前最新的放在一處，備份的放另一處
    3. 請大家討論一下
        - 第一個跟第二個有什麼好處？
        - 哪個比較好？
        - 有更好的嗎？
7. 將桌面分成兩部份:
    1. 一堆是改變迴紋針的地方，也就是工作目錄
    2. 一堆是放已經存檔的位置，也就是.git
8. 分享與討論

## 線
### 你會如何紀錄？
「你會如何紀錄？」是為了探討Git的物件特性與運作的方式，同時了解為何這麼做，並且比較「注重目錄變化」與「注重檔案變化」的差別比較。

**器材**  
- 很多大迴紋針
- 很多A4紙張
- 鉛筆、原子筆或者麥克筆
- 資料夾:L夾等可以裝文件的東西
- 資料櫃:可以裝很多資料夾的櫃子，沒有櫃子可以用資料夾

**時間**:依人數分配，以一小時為主。

**人數**  
無限制

**重點**
- 分享與討論
- 使用迴紋針模擬文字

**流程**
1. 每個人發一小袋迴紋針、數十張紙、三個資料夾
2. 將A4紙張依照說明折
3. 將迴紋針插入在對折處
4. 將他放入到資料夾內
5. 放入到櫃子，如果沒有櫃子沒關係，可以同一張桌子疊在一起
6. 問大家如果你要備份，你會怎麼用？
    1. 每一個備份一次，直接在資料夾所在位置
    2. 將目前最新的放在一處，備份的放另一處
    3. 請大家討論一下
        - 第一個跟第二個有什麼好處？
        - 哪個比較好？
        - 有更好的嗎？
7. 將桌面分成兩部份:
    1. 一堆是改變迴紋針的地方，也就是工作目錄
    2. 一堆是放已經存檔的位置，也就是.git

## 支
### 你會如何

名稱解釋:
- 印表機:製作快照與版本
- 物件:物件導向
- 文件搭配資料夾最終形成儲存庫

- 使用唯一標記

- 先以統一一個資料夾為主
- 再以很多資料夾分佈在不同人身上
- 工作目錄底下三個資料夾
- 三個資料夾統一記錄在紀錄紙上
- 大家用鉛筆寫，每次修改後擦掉修改成新的
- 有個起始文件
- 要編輯他，只有一張該怎麼辦
- 引導方式引導做法

遊戲介紹
- 請大家用迴紋針練習排列與放置:練習與學習使用，但不告訴他對應的是什麼。
- 請大家依序我講的將排列迴紋針
- 第五次時看大家能記得最新的嗎？
-

- 人寫一張，會發生什麼事？
- 再多人寫一張，會發生什麼事？
- 再發現只能放下一張，會發生什麼事？
- 那怎麼辦？你會怎麼做？
- 請回顧剛剛玩的過程中寫了什麼？發現什麼事情？
- 那怎麼辦？
- 會發生什麼事？

可能集中式:
- 每寫一次版本所有文件可以使用印表機複製一次
- 大家討論怎麼處理這件事
- 每人做一份副本
- 修改的內容如何合在一起
- 為每一次修改製作副本都作一次紀錄

可能分散式:
- 每寫一次版本所有文件可以使用印表機複製一次
- 大家討論怎麼處理這件事情
- 每人從基礎版本影印一份資料，並且依照此資料分別放置個人的資料夾(分支)
- 為每一次修改製作副本並加入描寫紀錄
- 以某個資料夾為基礎將大家合作的內容來合併檔案，完成製作



- 平均分配時間vs花費全部時間
- 如何解決製作太慢
- 加快製作流程
-
- Git基礎課程
- 印表機

- 在內湖
- 在金門測試
-
- 邀請一標加入
-
- 印表機
-
- 完成語法
- 完成記帳
-
- 遊戲版本物件導向
- 文件搭配資料夾最終形成儲存庫
- 使用唯一標記
- 使用列印機
- 先以統一一個資料夾為主
- 再以很多資料夾分佈在不同人身上
- 工作目錄底下三個資料夾
- 三個資料夾統一記錄在紀錄紙上
- 大家用鉛筆寫，每次修改後擦掉修改成新的
- 有個起始文件
- 要編輯他，只有一張該怎麼辦
- 引導方式引導做法
- 所有人寫一張，會發生什麼事？
- 再多人寫一張，會發生什麼事？
- 再發現只能放下一張，會發生什麼事？
- 那怎麼辦？你會怎麼做？
- 請回顧剛剛玩的過程中寫了什麼？發現什麼事情？
- 那怎麼辦？
- 會發生什麼事？

可能集中式:
- 每寫一次版本所有文件可以使用印表機複製一次
- 大家討論怎麼處理這件事
- 每人做一份副本
- 修改的內容如何合在一起
- 為每一次修改製作副本都作一次紀錄

可能分散式:
- 每寫一次版本所有文件可以使用印表機複製一次
- 大家討論怎麼處理這件事情
- 每人從基礎版本影印一份資料，並且依照此資料分別放置個人的資料夾(分支)
- 為每一次修改製作副本並加入描寫紀錄
- 以某個資料夾為基礎將大家合作的內容來合併檔案，完成製作