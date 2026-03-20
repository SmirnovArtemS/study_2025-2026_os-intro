---
## Front matter
title: "Индивидуальный проект. Этап 2"
subtitle: "Добавление данных о себе на персональный сайт"
author: "Смирнов Артём Сергеевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true
toc-depth: 2
lof: true
lot: true
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Добавить к персональному сайту данные о себе: разместить фотографию, написать краткую биографию, указать интересы и информацию об образовании, а также создать два поста.

# Задание

- Разместить фотографию владельца сайта
- Разместить краткое описание владельца сайта (Biography)
- Добавить информацию об интересах (Interests)
- Добавить информацию об образовании (Education)
- Сделать пост по прошедшей неделе
- Добавить пост на тему: Управление версиями. Git

# Теоретическое введение

Hugo Academic Theme (HugoBlox) использует систему профилей авторов для хранения информации о владельце сайта. Профиль автора хранится в файле `data/authors/me.yaml` и содержит структурированные данные: имя, биографию, аффилиации, интересы, образование и ссылки на социальные сети.

Блог-посты в Hugo размещаются в директории `content/blog/`. Каждый пост представляет собой папку с файлом `index.md`, содержащим метаданные (front matter) и текст статьи в формате Markdown.

Основные элементы профиля автора представлены в таблице [-@tbl:profile].

: Элементы профиля автора {#tbl:profile}

| Элемент | Описание |
|---------|----------|
| name | Имя автора (display, given, family) |
| role | Должность или статус |
| bio | Краткая биография |
| interests | Список интересов |
| education | Информация об образовании |
| links | Ссылки на социальные сети |

# Выполнение индивидуального проекта

## Размещение фотографии

Заменяю фотографию владельца сайта. Копирую своё фото в директорию `assets/media/authors/` с именем `me.jpg` (рис. -@fig:001).

![Размещение фотографии в директории проекта](image/1.png){#fig:001 width=70%}

## Обновление профиля автора

Открываю файл `data/authors/me.yaml` и заполняю информацию о себе (рис. -@fig:002).

Указываю следующие данные:

- **Имя**: Смирнов Артём Сергеевич
- **Роль**: Студент направления "Прикладная информатика"
- **Биография**: Студент РУДН, изучаю прикладную информатику и машинное обучение
- **Аффилиация**: РУДН

![Редактирование файла me.yaml](image/2.png){#fig:002 width=70%}

## Добавление интересов

В секции `interests` файла `me.yaml` добавляю список своих интересов (рис. -@fig:003):

- Программирование
- Веб-разработка 
- Машинное обучение
- Акробатика
- Спорт

![Добавление интересов в профиль](image/3.png){#fig:003 width=70%}

## Добавление информации об образовании

В секции `education` указываю информацию о своём образовании (рис. -@fig:004):

- Бакалавриат, Прикладная информатика
- Российский университет дружбы народов
- Факультет физико-математических и естественных наук
- Год начала обучения: 2025

![Добавление информации об образовании](image/4.png){#fig:004 width=70%}

## Создание поста о прошедшей неделе

Создаю директорию `content/blog/week-march-2026/` и файл `index.md` с постом о прошедшей неделе (рис. -@fig:005).

В посте описываю своё выступление на концерте в РУДН, где вместе с группой по английскому языку мы исполнили песню "In My Lonely Life" Лазарева.

![Создание поста о прошедшей неделе](image/5.png){#fig:005 width=70%}

## Создание поста про Git

Создаю директорию `content/blog/git-version-control/` и файл `index.md` с постом об управлении версиями с помощью Git (рис. -@fig:006).

В посте раскрываю следующие темы:
- Что такое Git
- Основные концепции (репозиторий, коммит, ветки)
- Базовые команды Git
- Рабочий процесс
- Лучшие практики

![Создание поста про Git](image/6.png){#fig:006 width=70%}

## Проверка результата

Запускаю локальный сервер Hugo командой `hugo server` и проверяю отображение изменений в браузере (рис. -@fig:007).

```bash
hugo server
```

![Проверка сайта на локальном сервере](image/7.png){#fig:007 width=70%}

Профиль отображается корректно с новой фотографией, биографией, интересами и образованием (рис. -@fig:008).

![Обновлённый профиль на сайте](image/8.png){#fig:008 width=70%}

Посты успешно отображаются в разделе блога (рис. -@fig:009).

![Посты в разделе блога](image/9.png){#fig:009 width=70%}

# Основные команды

Основные команды, использованные при выполнении проекта, представлены в таблице [-@tbl:commands].

: Основные команды {#tbl:commands}

| Команда | Описание |
|---------|----------|
| `cp photo.jpg assets/media/authors/me.jpg` | Копирование фотографии |
| `hugo server` | Запуск локального сервера разработки |
| `git add .` | Добавление всех изменений в индекс |
| `git commit -m "message"` | Создание коммита |
| `git push` | Отправка изменений на GitHub |

# Выводы

В ходе выполнения второго этапа индивидуального проекта добавил к персональному сайту данные о себе: разместил фотографию, заполнил биографию, указал интересы и информацию об образовании. Также создал два поста: о прошедшей неделе и на тему "Управление версиями. Git". Сайт успешно обновлён и доступен по адресу `https://SmirnovArtemS.github.io/`.

# Список литературы{.unnumbered}

::: {#refs}
:::
