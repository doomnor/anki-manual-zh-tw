# 新手上路 Getting Started

<!-- toc -->

## 安裝與升級 Installing & Upgrading

請參閱你的電腦系統的安裝指示：

- [Windows](./platform/windows/installing.md)
- [Mac](./platform/mac/installing.md)
- [Linux](./platform/linux/installing.md)

## 影片 Videos

以下影片將幫助你理解並上手使用 Anki。部分影片可能使用舊版 Anki，但概念是一樣的。(影片均為英文)

- [共用牌組和複習的基本操作](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on)

- [同步](https://www.youtube.com/watch?v=YkiM4DPzSVc&list=PLGgmaKOIHykFoomqkBJAyGiDQ2kyiuTao&yt:cc=on)

- [切換卡片順序](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

- [自訂卡片外觀](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

- [輸入回答問題](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

若你所在國家無法存取 YouTube，你可以[下載影片](https://apps.ankiweb.net/downloads/archive/screencasts/2.0/)。

## 核心概念 Key Concepts

### 卡片 Cards

一組問題和答案稱為一張「卡片」(card)。跟紙質的閃卡 (flashcard) 一樣，一面寫著問題，一面寫著答案。Anki 中的卡片看起來跟實體的卡片不一樣，並且使用預設設定時，你可以同時看到問題面和答案面。例如，若你在學習基礎化學，遇到以下問題：

    Q: 氧氣的化學符號？

經過思考，並得出答案為 O 後，你按下「顯示答案」按鈕，Anki 將顯示如下：

    Q: 氧氣的化學符號？
    A: O

確定你得出的是正確答案後，你可以告訴 Anki 你記住得有多牢，而 Anki 將決定該卡片下一次為你顯示的時間。

### 牌組 Decks

一個「牌組」(deck) 是一組卡片。你可以把卡片存放在不同的牌組中來學習你的集合 (collection) 中的一部分，而不是全部放在一起學習。每個牌組可以擁有不同的設定，例如每天要學習的新卡片，或是卡片再次出現的時機。

牌組可以包含子牌組，你可以用樹狀結構整理牌組。Anki 使用「::」來表示不同層級。牌組「英文::單字」表示「單字」牌組，它是「英文」牌組的一部分。若你選取「單字」，此時只有單字卡片會出現；若選「英文」，則全部的英文卡片，包括單字，將會出現。

要使用樹狀結構整理牌組，你可以在不同層級間加入「::」，或者在牌組列表中拖放牌組。在另一個牌組下的牌組 (即名稱中至少含有一個「::」的牌組)，常稱為子牌組 (subdeck)，而在上層的牌組有時稱為「superdeck」或「父牌組」(parent deck)。

一開始啟動 Anki 時，你將看到一個名為「default」的牌組；不包含於任何牌組的卡片將存放在那裡面。當 default 牌組中沒有卡片，且你已建立其他牌組時，Anki 會將其隱藏。另外，你也可以將它重新命名，並用來存放其他卡片。

牌組適合用來分類某一大類卡片，而不是細分為小話題——像是「食物類動詞」或「第1課」。若欲瞭解更多資訊，請參閱[恰當運用牌組 (Using Decks Appropriately)](editing.md#恰當運用牌組-using-decks-appropriately) 部分。

要瞭解更多關於牌組如何影響卡片出現順序的資訊，請見[顯示順序 (Display Order)](studying.md#顯示順序-display-order) 部分。

### 筆記與欄位 Notes & Fields

製作閃卡時，你經常會想要為某些資訊製作多張卡片。例如，若在學習法文時，你學到「bonjour」是「你好」的意思，你可能會想要建立一張卡片顯示「bonjour」讓你想出「你好」，再建立一張卡片顯示「你好」讓你想出「bonjour」。一張卡片測試你的被動認知能力，另一張卡片測試你的主動輸出能力。

使用紙質閃卡時，你唯一的辦法就是把同樣的資訊分別寫在兩張不同的卡片上。有些電腦閃卡程式提供在正面和背面之間翻轉的功能。比起紙質卡片，這無疑使你製作卡片輕鬆不少，但這樣做有兩個主要的缺點：

- 因為此類程式無法分開記錄你的認知和輸出表現，卡片經常不會在最佳的時機出現，這意味著你忘記內容的機會將增加，或者你可能會花費更多不必要的時間來學習。

- 翻轉問題和答案面僅適用於兩面完全一樣的內容。因此你沒有辦法在卡片的背面顯示額外的資訊，也沒有辦法實現其他類似的功能。

這些問題在 Anki 中得以解決，使用 Anki 時，你可以把卡片的內容分割成多則資訊。你可以告訴 Anki 你需要在哪張卡片上加入哪則資訊，Anki 就會幫你建立卡片，若你在未來編輯這些資訊，Anki 也會幫你更新。

假設現在你想要學習法文單字，而你想要在每張卡片的背面加入頁碼。你想要的卡片顯示效果如下：

    Q: Bonjour
    A: 你好
       第12頁

另一張卡片：

    Q: 你好
    A: Bonjour
       第12頁

在這個例子中，你有 3 則相關的資訊：一個法文單字、一個中文意思以及一個頁碼。把它們稍加整理，我們得到：

    法文: Bonjour
    中文: 你好
    頁碼: 12

在 Anki 中，這些關聯的資訊被稱為一則「筆記」(note)，每一則資訊被稱為一個「欄位」(field)。因此，我們可以說，這個筆記類型有 3 個欄位：法文、英文和頁碼。

要新增和編輯欄位，請在新增或編輯筆記時按一下「欄位...」(Fields…​) 按鈕。要進一步瞭解欄位，請參閱[自訂欄位 (Customizing Fields)](editing.md#自訂欄位-customizing-fields) 部分。

### 卡片類型 Card Types

要讓 Anki 按照我們的筆記內容來建立卡片，我們需要給它一張藍圖來告訴它，每張卡片的正反面需要顯示哪些欄位。我們把這張藍圖叫做「卡片類型」(card type)。每個筆記類型都可以擁有一或多個卡片類型；當你新增一則筆記時，Anki 就會為每一個卡片類型都建立一張卡片。

每一個卡片類型都有兩個「模板」(templates)，問題面和答案面分別一個。在上面的法文範例中，我們想讓被動認知卡片呈現以下效果：

    Q: Bonjour
    A: 你好
       第12頁

要達到這樣的效果，我們可以把問題和答案的模板設定成這樣：

    Q: {{法文}}
    A: {{中文}}<br>
       第{{頁碼}}頁

透過把欄位名稱寫在雙大括號內，我們告訴 Anki 用欄位內的實際資訊來取代這個部分。任何沒有寫在大括號裡的內容則保留原樣。（例如，我們不用每次加入材料時都輸入「第n頁」到頁碼欄位中——「第」和「頁」會被自動加入至每一張卡片中。）&lt;br&gt; 是一個特殊代碼，用來告訴 Anki 切換至下一行；請前往[模板 (Templates)](templates/intro.md) 部分瞭解更多資訊。

主動輸出卡片的卡片模板也類似：

    Q: {{中文}}
    A: {{法文}}<br>
       第{{頁碼}}頁

建立卡片類型後，每一次你新增一則筆記的同時，Anki 都將為其每一個卡片類型建立一張卡片。卡片類型使你得以輕鬆地統一每一張卡片的格式，讓你加入資訊時不再費時費力。並且，卡片類型使得 Anki 可以安排不讓關聯的卡片靠得太近；若你有錯字或其他錯誤，你只需要修改一次就可以套用到所有關聯的卡片上。

要新增和編輯卡片類型，請在新增或編輯筆記時按一下「卡片...」(Cards…​) 按鈕。要進一步瞭解卡片類型，請參閱[卡片和模板 (Cards and Templates)](templates/intro.md) 部分。

### 筆記類型 Note Types

在 Anki 中，你可以為不同的材料建立不同的筆記類型。每個筆記類型都有自己的欄位和卡片類型。在學習不同學科或主題時，不妨試著為每一門都分別建立一個筆記類型。在上面的法文範例中，我們可以建立一個名為「法文」的筆記類型。如果我們想要記住各國首都，就可以另外再建立一個筆記類型，欄位可以是「國家」和「首都」。

當 Anki 檢查重複項目時，它只會比較相同類型下的筆記。因此，若你在首都筆記類型中加入一個名為「橙子」的首都，等你要學習「橙子」在法文怎麼說時並不會看到重複訊息。

當你建立一個新集合時，Anki 會自動為其加入一些基本的筆記類型。這些筆記類型幫助新使用者更快上手 Anki，但要長期使用的話還是建議根據自己的學習內容來建立自己的筆記類型。以下是基本筆記類型：

**基本型 Basic** 
Has Front and Back fields, and will create one card. Text you enter in
Front will appear on the front of the card, and text you enter in Back
will appear on the back of the card.

**基本型 (含反向卡片) Basic (and reversed card)**  
Like Basic, but creates two cards for the text you enter: one from
front→back and one from back→front.

**基本型 (可選用反向卡片) Basic (optional reversed card)** 
This is a front→back card, and optionally a back→front card. To do this,
it has a third field called “Add Reverse.” If you enter any text into
that field, a reverse card will be created. More information about this
is available in the [Cards and Templates](templates/intro.md) section.

**克漏字 Cloze**  
A note type which makes it easy to select text and turn it into a cloze
deletion (e.g., “Man landed on the moon in \[…​\]” → “Man landed on the
moon in 1969”). More information is available in the [cloze
deletion](editing.md#cloze-deletion) section.

To add your own note types and modify existing ones, you can use Tools →
Manage Note Types from the main Anki window.

Notes and note types are common to your whole collection rather than
limited to an individual deck. This means you can use many different
types of notes in a particular deck, or have different cards generated
from a particular note in different decks. When you add notes using the
Add window, you can select what note type to use and what deck to use,
and these choices are completely independent of each other. You can also
change the note type of some notes [after you’ve already created
them](browsing.md).

### Collection

Your 'collection' is all the material stored in Anki – your cards,
notes, decks, note types, deck options, and so on.

## Shared Decks

You can watch [a video about Shared Decks and Review
Basics](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on) on YouTube.

The easiest way to get started with Anki is to download a deck of cards
someone has shared:

1. Click the “Get Shared” button at the bottom of the deck list.

2. When you’ve found a deck you’re interested in, click the “Download”
    button to download a deck package.

3. Double-click on the downloaded package to load it into Anki, or
    File→Import it.

Please note that it’s not currently possible to add shared decks
directly to your AnkiWeb account. You need to import them with the
desktop program, then synchronize to upload them to AnkiWeb.

Creating your own deck is the most effective way to learn a complex
subject. Subjects like languages and the sciences can’t be understood
simply by memorizing facts — they require explanation and context to
learn effectively. Furthermore, inputting the information yourself
forces you to decide what the key points are, leading to a better
understanding.

If you are a language learner, you may be tempted to download a long
list of words and their translations, but this won’t teach you a
language any more than memorizing scientific equations will teach you
astrophysics. To learn properly, you need textbooks, teachers, or
exposure to real-world sentences.

    Do not learn if you do not understand.
    --SuperMemo

Most shared decks are created by people who are learning material
outside of Anki – from textbooks, classes, TV, etc. They select the
interesting points from what they learn and put them into Anki. They
make no effort to add background information or explanations to the
cards, because they already understand the material. So when someone
else downloads their deck and tries to use it, they’ll find it very
difficult as the background information and explanations are missing.

That is not to say shared decks are useless – simply that for complex
subjects, they should be used as a 'supplement' to external material,
not as a 'replacement' for it. If you’re studying textbook ABC and
someone has shared a deck of ideas from ABC, that’s a great way to save
some time. And for simple subjects that are basically a list of facts,
such as capital city names or pub quiz trivia, you probably don’t need
external material. But if you attempt to study complex subjects without
external material, you will probably meet with disappointing results.
