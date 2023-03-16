---
title: "TDD與持續重構心得"
slug: tdd-and-refactor
date: 2023-03-05
categories:
- TDD
- Refactor
tags:
- TDD
- Refactor
thumbnailImagePosition: left
thumbnailImage: /images/tdd-cover.png
---


上個月參加 91 哥所開的 TDD 與持續重構課程，讓我更深入了解了測試驅動開發的概念和實踐方式。
雖然我在課前已經有一些 TDD 的經驗，但這門課讓我更有系統地學習了如何設計好的測試案例和依情境(不確定性)決定步伐大小，以及如何重構現有的代碼，進一步提升程式碼品質。
<!--more-->

在課程中，91哥扮演著需求方，提出一個 **模糊的** 需求，我們透過不斷的對話與提問，讓需求逐漸清晰，但現實是許多開發者一拿到需求，就想卯起來寫程式，過程中遇到不確定的問題，也是自行腦補、不斷通靈，那最後的成果可想而知，一定是失敗收尾，釐清需求後，我們才著手進行分組開發。

我最喜歡的一個部分是，在課程的結尾，我們學習了如何對**我們寫出來的 Legacy Code** 進行重構，
辨識 [Code Smells](https://refactoring.guru/refactoring/smells) 後，再透過[重構技巧](https://refactoring.guru/refactoring/techniques)去消除這些 [Code Smells](https://refactoring.guru/refactoring/smells) ，再萃取出領域物件，進而讓每個物件有各自的職責，過程中也運用到 IDE 很多的組合技，讓整個重構過程行雲流水，這種技能對於大多數公司需要維護和重構的 Legacy Code 來說非常實用。

最後再示範以 TDD 如何完成這項需求，先透過 IPO Model 初步分析可能的資訊有哪些，再設計出測試案例，每個案例都有它的意義，通常第一個都是 Happy Path，逼出需要的 Class 或 Method，盡可能讓每個案例需要做的事情單純，只做一件事，透過小步快跑，逐漸迭代來完善需求，寫的 Production Code 都是為了剛好滿足你測試的 Scenario，避免 Over Design，同時也保持 Simple Design ，但要注意的是 TDD 沒有教你如何怎麼設計，要設計出高品質的程式碼，仍需遵循 OO 和 SOLID，並將它們與 TDD 相結合，設計出具有高內聚、低耦合的程式碼。

要能在實務上靈活運用 TDD，絕對不是只要 Test-First 就好，設計測試案例的時候可以透過
UserStory 和 Specification by Example，在 TDD 的時候需要依情境決定步伐大小，重要的是需要具備 “**如何將顆粒度切小**” 的能力，才能化繁為簡，過程中也透過 IDE 提供的功能讓 IDE 幫你寫程式，讓省下的時間去思考如何將產品的設計品質提升。

如果在實務上你覺得很難直接運用 TDD，可以先從 [KATA](https://codingdojo.org/kata/) 的一些小型題目下手，從需求探索、實例化需求、單元測試、重構等等都可以練到，也可以找個夥伴進行 [Pair](https://medium.com/pm%E7%9A%84%E7%94%9F%E7%94%A2%E5%8A%9B%E5%B7%A5%E5%85%B7%E7%AE%B1/pair-programming-%E6%98%AF%E4%BB%80%E9%BA%BC-d4fffa7f0466)，透過反覆練習將這些技能內化，在實務上就能得心應手了。

Ref:  
[Code Smells](https://refactoring.guru/refactoring/smells)  
[Refactoring Techniques](https://refactoring.guru/refactoring/techniques)  
[Coding Dojo](https://codingdojo.org/kata/)

相關書籍:  
[Kent Beck 的測試驅動開發：案例導向的逐步解決之道](https://www.tenlong.com.tw/products/9789864345618)  
[使用者故事對照](https://www.tenlong.com.tw/products/9789863479468?list_name=srh)  
[Specification by Example 中文版：團隊如何交付正確的軟體](hhttps://www.tenlong.com.tw/products/9789862019481)  
[重構｜改善既有程式的設計, 2/e](https://www.tenlong.com.tw/products/9789865021832?list_name=srh)  
[管理、修改、重構遺留程式碼的藝術](https://www.tenlong.com.tw/products/9789864344000?list_name=srh)  
[無瑕的程式碼－敏捷完整篇－物件導向原則、設計模式與 C#實踐](https://www.tenlong.com.tw/products/9789864342099)