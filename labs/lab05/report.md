---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Продвинутое использование git"
author: "Дмитраков Михаил Алексеевич"

## Generic options
lang: ru-RU

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true
toc-title: Содержание
lof: true
lot: false
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

## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---

# Цель работы

Получение навыков правильной работы с репозиториями git.

# Теоретические сведения

Gitflow Workflow опубликована и популяризирована Винсентом Дриссеном. Gitflow Workflow предполагает выстраивание строгой модели ветвления с учётом выпуска проекта. Данная модель отлично подходит для организации рабочего процесса на основе релизов. Работа по модели Gitflow включает создание отдельной ветки для исправлений ошибок в рабочей среде.

Последовательность действий при работе по модели Gitflow:

- Из ветки master создаётся ветка develop.
- Из ветки develop создаётся ветка release.
- Из ветки develop создаются ветки feature.
- Когда работа над веткой feature завершена, она сливается с веткой develop.
- Когда работа над веткой release завершена, она сливается в ветки develop и master.
- Если в master обнаружена проблема, из master создаётся ветка hotfix.
- Когда работа над веткой hotfix завершена, она сливается в ветки develop и master.

## Общепринятые коммиты

Стандарт Conventional Commits — это простое соглашение о том, как следует формировать сообщение коммита. Он описывает простой набор правил для создания понятной истории коммитов, а также позволяет проще разрабатывать инструменты автоматизации, основанные на истории коммитов.

Структура сообщения коммита:

\`\`\`
<тип>[область]: <описание>

[тело]

[сноска(и)]
\`\`\`

# Выполнение лабораторной работы

## Работа с тестовым репозиторием

### Установка Node.js

Установил Node.js с помощью пакетного менеджера (рис. [-@fig:001]).

![Установка Node.js](image/1.png){#fig:001 width=70%}

### Настройка commitizen

Выполнил настройку commitizen для помощи в форматировании коммитов (рис. [-@fig:002]).

![Настройка commitizen](image/2.png){#fig:002 width=70%}

### Настройка standard-changelog

Выполнил настройку standard-changelog для автоматического создания логов (рис. [-@fig:003]).

![Настройка standard-changelog](image/3.png){#fig:003 width=70%}

### Создание package.json

Создал файл package.json с необходимой конфигурацией для работы с conventional commits (рис. [-@fig:004]).

![Создание package.json](image/4.png){#fig:004 width=70%}

### Использование commitizen

Выполнил коммит с помощью commitizen, используя команду cz-conventional-changelog (рис. [-@fig:005]).

![Использование commitizen](image/5.png){#fig:005 width=70%}

### Инициализация git-flow

Инициализировал git-flow в тестовом репозитории (рис. [-@fig:006]).

![Инициализация git-flow](image/6.png){#fig:006 width=70%}

### Завершение релиза

Завершил релиз в тестовом репозитории с помощью git-flow (рис. [-@fig:007]).

![Завершение релиза](image/7.png){#fig:007 width=70%}

### Отправка на GitHub

Отправил изменения на GitHub, включая все ветки и теги (рис. [-@fig:008]).

![Отправка на GitHub](image/8.png){#fig:008 width=70%}

### Объединение веток

Выполнил объединение веток develop и master (рис. [-@fig:009]).

![Объединение веток](image/9.png){#fig:009 width=70%}

### Завершение релиза

Завершил релиз и отправил результаты на GitHub (рис. [-@fig:010]).

![Завершение релиза](image/10.png){#fig:010 width=70%}

## Подготовка рабочего репозитория

### Создание package.json и коммит

Создал файл package.json в рабочем репозитории и выполнил коммит (рис. [-@fig:011]).

![Подготовка рабочего репозитория — package.json и коммит](image/11.png){#fig:011 width=70%}

### Завершение релиза

Завершил релиз в рабочем репозитории (рис. [-@fig:012]).

![Подготовка рабочего репозитория — завершение релиза](image/12.png){#fig:012 width=70%}

# Вывод

В ходе выполнения данной лабораторной работы я получил навыков правильной работы с репозиториями git, освоил модель Gitflow, научился использовать conventional commits с помощью commitizen и standard-changelog.
