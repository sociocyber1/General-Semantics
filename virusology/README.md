# Вирусо-логия семантических реакций

**Общая семантика: наука человеческих оценок.**
SocioCyberneering Inc. · [sociocyber.site](https://sociocyber.site) · [github.com/sociocyber1](https://github.com/sociocyber1)

Документ о том, как слова, ярлыки и оценки работают как вирусы: меняют реакции человека в обход сознательного анализа. Основан на идеях Альфреда Коржибски (*«Наука и Здравомыслие»*, 1933) и Уэнделла Джонсона (цикл ИФД).

Языки: русский (`virusology.pdf`) и английский (`virusology_en.pdf`, English edition). Версия: 0.8. Статус: рабочий черновик, возможны ошибки, примеры и поправки приветствуются.

## Что внутри

| Часть | Содержание |
|---|---|
| **Часть I** | Вирусо-логия семантических реакций: болезнь ИФД, перехват коры амигдалой, инъекция семантических реакций (`[SRI]`), каталог атак (`[MAP Spoofing]`, `[GRB]`, `[EDC]`, `[Rootkit]` и другие), сверка карты и территории |
| **Часть II** | Вирусология оценок: школа как точка передачи. Оценка как ярлык личности, публичное унижение как `[E.A.Alert]`, зубрёжка как `[EDC]`, ярлык «лень», патриотизм как `[Rootkit]`, антивирус |
| **Схемы** | Шесть схем в стиле «Доски Мерсера»: цикл ИФД, перехват коры, лестница абстракций, причины за ярлыком «лень», цепочка заражения, пауза-антивирус |
| **Глоссарий** | Все термины: код, английское название, перевод на русский, описание. Коды в тексте кликабельны и ведут в глоссарий |
| **Приложение** | «Решение-проблем. Рабочая тетрадь»: шесть шагов от проблемы к действию (PDF встроен целиком) |

## Главная мысль

Ярлык вместо описания события это **`[MAP Spoofing]`**: подмена карты. «Лени не существует»: за ярлыком всегда стоит конкретная причина (нет метода, нет смысла, страх ошибки, истощение), а значит, нужен **инструмент вместо ярлыка**, пауза вместо рефлекса и вопрос вместо крика.

## Структура репозитория

```
virusology/
├── virusology.tex            исходник (XeLaTeX + polyglossia)
├── virusology.pdf            собранный документ (русский)
├── virusology_en.tex         English edition: исходник
├── virusology_en.pdf         English edition: собранный документ
├── fonts/                    статичные Montserrat (Regular, SemiBold, Bold)
├── appendix/
│   └── problem_solving_ru.pdf  рабочая тетрадь, встраивается в конец
└── README.md
```

## Как собрать

Нужны TeX Live с XeLaTeX и пакеты `polyglossia`, `fontspec`, `tikz`, `mdframed`, `pdfpages`, `hyperref`. Шрифты: Liberation Serif, DejaVu Sans Mono (системные) и Montserrat (лежит в `fonts/`).

```bash
cd virusology
xelatex virusology.tex
xelatex virusology.tex   # второй проход: оглавление и ссылки
# English edition: то же для virusology_en.tex
```

Montserrat подключается из `fonts/` как статичный файл. Variable-версия шрифта не подходит: XeTeX берёт из неё самое тонкое начертание.

## Оформление

- Рамки по смыслу: синяя `механизм`, красная `опасность`, зелёная `инструмент`, золотая `пример`.
- Кавычки красные: `'слово'`.
- Тонкие начертания не используются: только Regular и Bold.

## Лицензия

GPL-3.0. Автор: SocioCyberneering Inc.

> Не используй меня во вред. Материалы предназначены для защиты от семантических атак, а не для манипуляции людьми.


---

## English

**The Virology of Semantic Reactions**: general semantics applied to how words, labels and evaluations act like viruses on human reactions (after Alfred Korzybski and Wendell Johnson). Part I covers the mechanics (IFD cycle, amygdala bypass, semantic reaction injection, attack catalogue). Part II applies it to school: grades as labels, public humiliation as an amygdala trigger, rote learning as data corruption, the label "laziness" as map spoofing, and the antivirus. Includes six diagrams and a clickable glossary. The appendix (a problem-solving workbook) is embedded in its Russian original.

Build: `xelatex virusology_en.tex` twice. Licence: GPL-3.0; Montserrat is under the SIL OFL 1.1.
