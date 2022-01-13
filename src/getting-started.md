# 新手上路 Getting Started

<!-- toc -->

## 安裝與升級 Installing & Upgrading

請參閱你的電腦系統的安裝指示：

- [Windows](./platform/windows/installing.md)
- [Mac](./platform/mac/installing.md)
- [Linux](./platform/linux/installing.md)

## 影片 Videos

以下影片將幫助您理解並上手使用 Anki。部分影片可能使用舊版 Anki，但概念是一樣的。
(影片均為英文)

- [共用牌組和複習的基本操作](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on)

- [同步](https://www.youtube.com/watch?v=YkiM4DPzSVc&list=PLGgmaKOIHykFoomqkBJAyGiDQ2kyiuTao&yt:cc=on)

- [切換卡片順序](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

- [自訂卡片外觀](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

- [輸入回答問題](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

若你所在國家無法存取 YouTube，你可以[下載影片](https://apps.ankiweb.net/downloads/archive/screencasts/2.0/)。

## 核心概念 Key Concepts

### 卡片 Cards

一組問題和答案稱為一張「卡片」(card)。跟紙質的閃卡 (flashcard) 一樣，一面
寫著問題，一面寫著答案。Anki 中的卡片看起來跟實體的卡片不一樣，並且使用預設
設定時，你可以同時看到問題面和答案面。例如，若你在學習基礎化學，遇到以下問題：

    Q: 氧氣的化學符號？

經過思考，並得出答案為 O 後，你按下「顯示答案」按鈕，Anki 將顯示如下：

    Q: 氧氣的化學符號？
    A: O

確定你得出的是正確答案後，你可以告訴 Anki 你記住得有多牢，而 Anki 將決定
該卡片下一次為你顯示的時間。

### 牌組 Decks

一個「牌組」(deck) 是一組卡片。你可以把卡片存放在不同的牌組中來學習你的
集合 (collection) 中的一部分，而不是全部放在一起學習。每個牌組可以擁有不同的
設定，例如每天要學習的新卡片，或是卡片再次出現的時機。

牌組可以包含子牌組，你可以用樹狀結構整理牌組。Anki 使用「::」來表示不同層級。
牌組「英文::單字」表示「單字」牌組，它是「英文」牌組的一部分。若你選取「單字」，
此時只有單字卡片會出現；若選「英文」，則全部的英文卡片，包括單字，將會出現。

要使用樹狀結構整理牌組，你可以在不同層級間加入「::」，或者在牌組列表中拖放牌組。
在另一個牌組下的牌組 (即名稱中至少含有一個「::」的牌組)，常稱為子牌組 (subdeck)，
而在上層的牌組有時稱為「superdeck」或「父牌組」(parent deck)。

一開始啟動 Anki 時，你將看到一個名為「default」的牌組；不包含於任何牌組的卡片
將存放在那裡面。當 default 牌組中沒有卡片，且你已建立其他牌組時，Anki 會將其隱藏。
另外，你也可以將它重新命名，並用來存放其他卡片。

Decks are best used to hold broad categories of cards, rather than
specific topics such as “food verbs” or “lesson 1”. For more info on
this, please see the [using decks appropriately](editing.md#using-decks-appropriately) section.

For information on how decks affect the order cards are displayed in,
please see the [display order](studying.md#display-order) section.

### Notes & Fields

When making flashcards, it’s often desirable to make more than one card
that relates to some information. For example, if you’re learning
French, and you learn that the word “bonjour” means “hello”, you may
wish to create one card that shows you “bonjour” and asks you to
remember “hello”, and another card that shows you “hello” and asks you
to remember “bonjour”. One card is testing your ability to recognize the
foreign word, and the other card is testing your ability to produce it.

When using paper flashcards, your only option in this case is to write
out the information twice, once for each card. Some computer flashcard
programs make life easier by providing a feature to flip the front and
back sides. This is an improvement over the paper situation, but there
are two major downsides:

- Because such programs don’t track your performance of recognition
  and production separately, cards will tend not to be shown to you at
  the optimum time, meaning you forget more than you’d like, or you
  study more than is necessary.

- Reversing the question and answer only works when you want exactly
  the same content on each side. This means it’s not possible to
  display extra info on the back of each card for example.

Anki solves these problems by allowing you to split the content of your
cards up into separate pieces of information. You can then tell Anki
which pieces of information you want on each card, and Anki will take
care of creating the cards for you and updating them if you make any
edits in the future.

Imagine we want to study French vocabulary, and we want to include the
page number on the back of each card. We want our cards to look like
this:

    Q: Bonjour
    A: Hello
       Page #12

And:

    Q: Hello
    A: Bonjour
       Page #12

In this example, we have three pieces of related information: a French
word, an English meaning, and a page number. If we put them together,
they’d look like this:

    French: Bonjour
    English: Hello
    Page: 12

In Anki, this related information is called a 'note', and each piece of
information is called a 'field'. So we can say that this type of note
has three fields: French, English, and Page.

To add and edit fields, click the “Fields…​” button while adding or
editing notes. For more information on fields, please see the
[Customizing Fields](editing.md#customizing-fields) section.

### Card Types

In order for Anki to create cards based on our notes, we need to give it
a blueprint that says which fields should be displayed on the front or
back of each card. This blueprint is called a 'card type'. Each type of
note can have one or more card types; when you add a note, Anki will
create one card for each card type.

Each card type has two 'templates', one for the question and one for the
answer. In the above French example, we wanted the recognition card to
look like this:

    Q: Bonjour
    A: Hello
       Page #12

To do this, we can set the question and answer templates to:

    Q: {{French}}
    A: {{English}}<br>
       Page #{{Page}}

By surrounding a field name in double curly brackets, we tell Anki to
replace that section with the actual information in the field. Anything
not surrounded by curly brackets remains the same on each card. (For
instance, we don’t have to type “Page \#” into the Page field when
adding material – it’s added automatically to every card.) &lt;br&gt; is
a special code that tells Anki to move to the next line; more details
are available in the [templates](templates/intro.md) section.

The production card templates work in a similar way:

    Q: {{English}}
    A: {{French}}<br>
       Page #{{Page}}

Once a card type has been created, every time you add a new note, a card
will be created based on that card type. Card types make it easy to keep
the formatting of your cards consistent and can greatly reduce the
amount of effort involved in adding information. They also mean Anki can
ensure related cards don’t appear too close to each other, and they
allow you to fix a typing mistake or factual error once and have all the
related cards updated at once.

To add and edit card types, click the “Cards…​” button while adding or
editing notes. For more information on card types, please see the [Cards
and Templates](templates/intro.md) section.

### Note Types

Anki allows you to create different types of notes for different
material. Each type of note has its own set of fields and card types.
It’s a good idea to create a separate note type for each broad topic
you’re studying. In the above French example, we might create a note
type called “French” for that. If we wanted to learn capital cities, we
could create a separate note type for that as well, with fields such as
“Country” and “Capital City”.

When Anki checks for duplicates, it only compares other notes of the
same type. Thus if you add a capital city called “Orange” using the
capital city note type, you won’t see a duplicate message when it comes
time to learn how to say “orange” in French.

When you create a new collection, Anki automatically adds some standard
note types to it. These note types are provided to make Anki easier for
new users, but in the long run it’s recommended you define your own note
types for the content you are learning. The standard note types are as
follows:

**Basic** 
Has Front and Back fields, and will create one card. Text you enter in
Front will appear on the front of the card, and text you enter in Back
will appear on the back of the card.

**Basic (and reversed card)**  
Like Basic, but creates two cards for the text you enter: one from
front→back and one from back→front.

**Basic (optional reversed card)** 
This is a front→back card, and optionally a back→front card. To do this,
it has a third field called “Add Reverse.” If you enter any text into
that field, a reverse card will be created. More information about this
is available in the [Cards and Templates](templates/intro.md) section.

**Cloze**  
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
