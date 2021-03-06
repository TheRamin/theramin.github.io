---
layout: post
title: "Про markdown"
date: 2021-10-19 22:20:32 +1000
category: IT
tags: markup-language markdown
---
Markdown - это очень лёгкий язык разметки, который из-за своей простоты очень легко перевести в html, с которым уже можно спокойно работать на сайтах.

Эта статья о том, что есть в markdown и как это применять.

# Оглавление
 - [Горизонтальные линии](#lines)
 - [Манипуляции с текстом](#text)
 - [Заголовки](#headers)
 - [Ссылки](#links)
 - [Картинки](#images)
 - [Цитаты](#blockquotes)
 - [Списки](#lists)
 - [Абзацы](#paragraphs)
 - [Блоки кода](#code)
 - [Ссылки на переход по коду](#links_to_smth)

## Горизонтальные линии<a name="lines"></a>
Горизонтальные линии делаются просто, нужно просто записать три или больше кое-каких символов, а именно дефисы(-), нижние подчёркивания(_) и звёздочки(*)

```markdown
---
```
---
<br>
```markdown
___
```
___
<br>
```markdown
***
```
***

## Манипуляции с текстом<a name="text"></a>
Чтобы выделить текст курсивом можно обрамить его в нижнее подчёркивание(_)

```markdown
_Курсив_ 
```

_Курсив_

Чтобы сделать текст жирным, нужно обрамить его в две звёздочки(**)

```markdown
**Жирный**
```

**Жирный**

VNIMANIE: автор не хочет указать на жирность этих слов, тем самым показывая свою нетерпимость по отношению к ним, автор не словофоб, любите и цените друг друга!

Также вы можете сделать текст одновременно и курсивным и жирным, просто обрамив текст в две звёздочки и в нижнее подчёркивание

```markdown
**_Жирный и курсивный текст_**
```

**_Жирный и курсивный текст_**

Причём неважно в каком порядке

```markdown
_**Жирный и курсивный текст**_
```

_**Жирный и курсивный текст**_

## Заголовки<a name="headers"></a>
Ну тут всё просто, любой заголовок начинается с хеш-тега(#) и "уровень" заголовка зависит от количества # перед ним, всего может быть 6 уровней

```markdown
# Заголовок 1-го уровня
```

# Заголовок 1-го уровня

```markdown
## Заголовок 2-го уровня
```

## Заголовок 2-го уровня

```markdown
### Заголовок 3-го уровня
```

### Заголовок 3-го уровня

```markdown
#### Заголовок 4-го уровня
```

#### Заголовок 4-го уровня

```markdown
##### Заголовок 5-го уровня
```

##### Заголовок 5-го уровня

```markdown
###### Заголовок 6-го уровня
```

###### Заголовок 6-го уровня

Заголовки нельзя сделать жирными, если мы их обрамим в двойные звёздочки(**), то ничего не произойдёт, но заголовки можно сделать курсивными, вот, например, курсивный заголовок 3-го уровня:

```markdown
### _Курсивный заголовок 3-го уровня_
```

### _Курсивный заголовок 3-го уровня_

## Ссылки<a name="links"></a>
Ссылки являются наиглавнейшим инструментом в интернете, без которых много обыденных нам вещей просто бы не было, поэтому и в markdown ссылки естественно есть

Самая обычная ссылка в markdown делается так: \[текст ссылки в квадратных скобках](и ресурс, на который будет вести ссылка), вот, например

```markdown
[Ссылка на GitHub репозиторий ядра linux](https://github.com/torvalds/linux)
```

[Ссылка на GitHub репозиторий ядра linux](https://github.com/torvalds/linux)

Естественно и жирность, и курсив для текста ссылки будет применяться

```markdown
[_Ссылочка_ **на** **_YouTube_**](https://youtube.com)
```

[_Ссылочка_ **на** **_YouTube_**](https://youtube.com)

Ещё ссылку можно поместить в заголовок

```markdown
#### [Поиграем в настолки?](https://boardgamearena.com/)
```

#### [Поиграем в настолки?](https://boardgamearena.com/)

Ещё ссылки можно сделать по другому, нужно просто также записать [текст ссылки в квадратных скобках] и после этого тоже в квадратных скобках [записать "аннотацию" на ссылку], а ниже записать ссылку, которая будет замещена на эту "аннотацию". Знаю, выглядит сложно, но на примере намного легче, вот, на пример, та же ссылка на ядро Линукса и на ютуб, только в виде "аннотаций"

```markdown
[Ссылка на GitHub репозиторий ядра linux][linux rep]
```

[Ссылка на GitHub репозиторий ядра linux][linux rep]

```markdown
[_Ссылочка_ **на** **_YouTube_**][youtube]
```

[_Ссылочка_ **на** **_YouTube_**][youtube]

И главное не забыть написать ссылку, которая будет в аннотации

```markdown
[linux rep]: https://github.com/torvalds/linux
[youtube]: https://youtube.com
```
	
[linux rep]: https://github.com/torvalds/linux  
[youtube]: https://youtube.com

## Картинки<a name="images"></a>
В markdown можно легко добавлять картинки, учитывая то, что их синтаксис схож с ссылками, например, картинки тоже можно записать с помощью аннотаций. Разница лишь в том, что перед картинками стоит восклицательный знак(!)

Вот, например, как добавить картинку octocat из сети в markdown

```markdown
![Маскот GitHub](https://github.githubassets.com/images/modules/logos_page/Octocat.png)
```

![Маскот GitHub](https://github.githubassets.com/images/modules/logos_page/Octocat.png)

Также можно добавлять и локальные файлы, указывая к ним относительный, или полный путь в системе, например, вот локальнй файл из репозитория, где расположен этот блог

```markdown
![Everlasting summer](/media/everlasting_summer.png)
```

![Everlasting summer](/media/everlasting_summer.png)

Естественно эти примеры можно записать и через аннотации, просто записав их на месте ссылок

```markdown
![Маскот GitHub][octocat]  
![Everlasting summer][summer without end]

[octocat]: https://github.githubassets.com/images/modules/logos_page/Octocat.png  
[summer without end]: /media/everlasting_summer.png
```

## Цитаты<a name="blockquotes"><a>
В markdown очень просто сделать цитату, просто поставьте перед текстом цитаты знак больше(>). Да, это всё

```markdown
> «Я не согласен ни с одним словом, которое вы говорите, но готов умереть за ваше право это говорить»   
>  
>_Эвелин Холл_
```

> «Я не согласен ни с одним словом, которое вы говорите, но готов умереть за ваше право это говорить» 
>
>_Эвелин Холл_

И да, чтобы записать цитату в несколько строк, нужно просто написать ещё один (>) после следующей строки, что будет означать перевод коретки, ну или клавишу Enter, как хотите

Также цитаты могут содержать и другие элементы markdown, такие как курсив(который я использовал в примере) или даже ихображения и ссылки соответственно

## Списки<a name="lists"></a>
Ну тут всё предельно просто

Ненумированые списки объявляются так(их ещё можно определять плюсиком(+) и звёздочкой(*))

```markdown
- первый пункт
- второй пункт
- третий пункт
```

- первый пункт
- второй пункт
- третий пункт

Нумерованные списки обозначаются ещё проще

```markdown
1. Первый пункт
2. Второй пункт
3. третий пункт
```

1. Первый пункт
2. Второй пункт
3. третий пункт

Также можно сделать и вложенные и комбинированные списки, и добавлять другие элементы markdown, например

```markdown
1. Первый пункт  
  - Первый вложенный пункт первого __пункта_  
  - Второй вложенный пункт **первого** пункта  
2. Второй пункт  
  - Первый [вложенный](https://google.com) пункт второго пункта
```


1. Первый пункт
  - Первый вложенный пункт первого __пункта_
  - Второй вложенный пункт **первого** пункта
2. Второй пункт
  - Первый [вложенный](https://google.com) пункт второго пункта

## Абзацы<a name="paragraphs"></a>

В markdown немного специфичная система абзацов, если вы напишете какой-то текст и нажмёте Enter один раз, перейда на другую строку и написав текст там, вы заметите, что текст-то остался в одной строке. Дело в том, что для того, чтобы перевести коретку или начать новый абзац нужно сделать немного неочевидные вещи

Для того, чтобы начать текст с новой строки, нужно в конце первой строки прописать два пробела, вот так(пробелы обозначены звёздочками)

```
Какой-то текст**  
И ещё какой-то текст**  
Ну ещё чуточку текста
```

Какой-то текст  
И ещё какой-то текст  
Ну ещё чуточку текста

А чтобы Начать новый параграф нужно просто нажать Enter два раза(пустая строка показана точкой)

```
Какой-то текст  
.  
И ещё какой-то текст  
.   
Ну ещё чуточку текста
```

Какой-то текст

И ещё какой-то текст

Ну ещё чуточку текста

## Блоки кода<a name="code"></a>

Блоки кода по стандарту поддерживаются, но не подсветка синтаксиса, например GitHub может и подсветку синтаксиса подключать

В общем, чтобы сделать блок кода, ножно просто обернуть его в три обратных апострафа(```) и записать тип синтаксиса, который будет подсвечен(ну или ничего не писать, просто чтобы был блок кода), например немного кода на питоне

```python
hello = "hello"

print(hello, "world")
```

## Ссылки на переход по коду<a name="links_to_smth"></a>

В markdown можно делать ссылки на переход к элементам внутри markdown кода, это можно сделать за счёт поддержки некоторого количества html тегов, в том числе тега \<a>, это тег ссылки, и у него есть атрибут "name", если незнаете, что такое html вообще, загуглите, не маленькие, в общем присвоя имя тегу ссылки, можно сделать ссылку уже на него внутри markdown, вот, например, как сделано оглавление в этой статье:

```markdown
 - [Горизонтальные линии](#lines)
 - [Манипуляции с текстом](#text)
 - [Заголовки](#headers)
 - [Ссылки](#links)
 - [Картинки](#images)
 - [Цитаты](#blockquotes)
 - [Списки](#lists)
 - [Абзацы](#paragraphs)
 - [Блоки кода](#code)
 - [Ссылки на переход по коду](#links_to_smth)
```

Т.е. мы после каждого заголовка можем написать тег \<a> и присвоить ему своё имя, вот так:

```
## Горизонтальные линии<a name="lines"></a>
```

И когда мы будем нажимать на ссылку в оглавлении нас будет перекидывать на этот заголовок, вот так вот просто