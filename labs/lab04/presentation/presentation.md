---
## Front matter
lang: ru-RU
title: Лабораторная работа №4
subtitle: Операционные системы
author:
  - Смирнов А. С.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 6 марта 2026

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
  - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- Смирнов Артём Сергеевич
- Студент группы НПИбд-02-25
- Российский университет дружбы народов
- [1032252364@rudn.ru](mailto:1032252364@rudn.ru)

:::
::: {.column width="30%"}

![](./image/photo.png)

:::
::::::::::::::

# Цель работы

Получение навыков правильной работы с репозиториями git.

# Задание

- Выполнить работу для тестового репозитория
- Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits

# Выполнение лабораторной работы

## Установка git-flow

Устанавливаю git-flow из коллекции репозиториев Copr.

![Установка git-flow](./image/1.png){#fig:001 width=60%}

## Установка Node.js и pnpm

Устанавливаю Node.js и pnpm для работы с инструментами версионирования.

![Установка Node.js и pnpm](./image/2.png){#fig:002 width=60%}

## Установка commitizen

Устанавливаю commitizen, cz-conventional-changelog и standard-changelog.

![Установка пакетов](./image/4.png){#fig:003 width=60%}

## Создание репозитория на GitHub

Создаю новый публичный репозиторий git-extended на GitHub.

![Репозиторий на GitHub](./image/5.png){#fig:004 width=60%}

## Настройка package.json

Инициализирую pnpm и добавляю конфигурацию commitizen в package.json.

![Содержимое package.json](./image/8.png){#fig:005 width=60%}

## Первый коммит через git cz

Выполняю коммит через интерактивный интерфейс git cz.

![Интерфейс git cz](./image/9.png){#fig:006 width=60%}

## Инициализация git-flow

Инициализирую git-flow с префиксом тегов `v`.

![Инициализация git-flow](./image/11.png){#fig:007 width=60%}

## Проверка ветки

Проверяю, что нахожусь на ветке develop.

![Проверка ветки](./image/12.png){#fig:008 width=60%}

## Создание релиза 1.0.0

Создаю ветку релиза и генерирую CHANGELOG.md.

![Создание релиза 1.0.0](./image/14.png){#fig:009 width=60%}

## Журнал изменений

Создаю CHANGELOG.md с помощью standard-changelog.

![CHANGELOG.md](./image/15.png){#fig:010 width=60%}

## Релиз на GitHub

Создаю релиз v1.0.0 на GitHub.

![Страница релизов](./image/18.png){#fig:011 width=60%}

## Feature-ветка

Создаю feature-ветку и добавляю новый функционал.

![Создание feature-ветки](./image/19.png){#fig:012 width=60%}

## Коммит нового функционала

Выполняю коммит через git cz с типом feat.

![Коммит через git cz](./image/20.png){#fig:013 width=60%}

## Создание релиза 1.2.3

Создаю новый релиз и обновляю версию в package.json.

![Создание релиза 1.2.3](./image/22.png){#fig:014 width=60%}

## Оба релиза на GitHub

Проверяю страницу релизов — доступны оба релиза v1.0.0 и v1.2.3.

![Страница релизов с обоими релизами](./image/27.png){#fig:015 width=60%}

# Выводы

В ходе выполнения лабораторной работы получил навыки правильной работы с репозиториями git. Освоил методологию Gitflow Workflow и спецификацию Conventional Commits. Научился использовать commitizen и standard-changelog для автоматизации процесса разработки.
