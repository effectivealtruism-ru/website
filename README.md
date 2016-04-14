# Сайт effectivealtruism.ru

[![Build Status](https://travis-ci.org/effectivealtruism-ru/website.svg?branch=master)](https://travis-ci.org/effectivealtruism-ru/website)

Сайт сделан на движке [Lektor](https://www.getlektor.com/), это такой генератор статических сайтов. Шаблоны для генерации сайта находятся в этом бранче. В бранче `gh-pages` - статический html, который выкладывается на Github Pages командой `lektor deploy`.

# Как что-то поправить

## С настройкой среды разработки

1. Установите [Lektor](https://www.getlektor.com/docs/installation/)
2. Форкните репозиторий и скачайте локальную рабочую копию.
3. Запустите `lektor server`.
4. Откройте [localhost:5000](http://localhost:5000), нажмите на карандаш в правом верхнем углу, и исправляйте что угодно. Или просто исправляйте код в любом текстовом редакторе.
5. Проверьте, что изменения выглядят так, как вы хотели, и присылайте pull request.

## Я не умею писать код, и просто хочу поправить тексты!

Зайдите в директорию [content](https://github.com/effectivealtruism-ru/website/tree/master/content). В ней есть иерархия директорий, соответствующая структуре сайта.

В файлах `contents.lr` находится текстовое описание страниц. Найдите тот, который вы хотите поправить, и нажмите иконку `"Edit this file"` в правом верхнем углу:

<img src='http://effectivealtruism.ru/static/github-edit-tutorial.png' width='372' height='237' alt='Иконка Edit this site' />

(Если всплывающая подсказка на иконке говорит `"You must be signed in to make or propose changes"`, сначала зарегистрируйтесь или залогиньтесь на github'е.)

Отредактируйте то, что нужно, и нажмите большую зелёную кнопку `"Propose file change"` внизу.

Готово! В репозитории будет создан pull request (запрос на внесение изменений), мы его проверим и добавим на сайт.

# Технические подробности

## Как происходит выкладывание новых версий на сайт?

Как только код попадает в master-бранч, запускается автоматическая сборка в [Travis CI](https://travis-ci.org/effectivealtruism-ru/website). Если она проходит успешно, то сайт обновляется автоматически.
