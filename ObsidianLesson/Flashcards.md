
#addon #tool #Obsidian 
Obsidian 联动 [[Anki]] 插件，通过使用特定语法，一键将文档中的内容制成 Anki 卡片进行定期回顾。
现已支持
	🔢 Support for **LaTeX**  
	🖼️ Support for **images**  
	🎤 Support for **audios**  
	🔗 Support for **Obsidian URI**  
	⚓ Support for **reference to note**  
	📟 Support for **code syntax highlight**


🗃️ Simple flashcards with #card
🎴 Reversed flashcards with #card-reverse or #card/reverse
📅 Spaced-only cards with #card-spaced or #card/spaced
✍️ Inline style with Question::Answer
✍️ Inline style reversed with Question:::Answer
📃 Cloze with Highlight or {Curly brackets} or {2: Cloze}
🧠 Context-aware mode
🏷️ Global and local tags

## 使用方法

Git 地址：[GitHub - reuseman/flashcards-obsidian: 🎴 An Anki plugin for Obsidian.md](https://github.com/reuseman/flashcards-obsidian)

## 生成卡片

### 标签法
插件会自动识别标签—— #card 
在标题行和内容行中间插入 #card 标签即可
此时**标题**为卡面，**内容**为卡背（**PS** 当内容中含有空行时，卡背内容会在空行处停止截取）
```
# This could be a title

## This is the front #card    
This is the back of the card.

This line will not be part of it, because there is an empty line above.

### This is a normal and reversed card #card-reverse
Which means that two cards will be generated on Anki.

### Also revers #card/reverse
But this time it uses Obsidian hierarchical tags.

### This could be another question #card
But this time without the heading.

## This is another way to define the front
#card 
This style is usefull to avoid the hashtags when referencing in Obsidian

```

### 双冒号法
在**同一行内**，**卡面内容** :: **卡背内容**
**PS** 需要使用英文冒号即半角冒号才能识别。可以通过使用 [[Easy Typing]] 插件自动将输入的两个中文冒号转换为一个英文冒号（即输入四次中文冒号）
```
# This could be a title

All of these works:
My question::My answer
My question:: My answer
My question ::My Answer
My question :: My answer

You can even use it in lists:
- My question:: My answer
```
三冒号生成正反卡

### 高亮法
插件会识别一行内含在**一对双等号**的内容识别为**填空题**
```
This is a way to define a ==cloze== by using the Obsidian highlight syntax in order to avoid making notes dirty.
The alternative is this type of {cloze} that is totally equal to {1:cloze}. With the number you can specify the order {2:later cloze}.
```

## 标签
