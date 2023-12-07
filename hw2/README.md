# Шаги

## Выбрали `git-lfs` как систему управления крупными файлами

## Устанавливаем `git-lfs`

```bash
yay -S git-lfs
```

## Инициалиизируем `git-lfs` внутри проекта

```bash
git lfs install
```

## Добавляем файлы `*.csv` для наблюдения

```bash
git lfs track "*.csv"
```

Автоматически добавился файл `.gitattributes`

`*.csv filter=lfs diff=lfs merge=lfs -text`

## Если хотим добавить - стандартный подход

```bash
git add imdb.csv
git commit -m "added imdb dataset"
```

## Копирование удаленного проекта локально

```bash
git pull
git lfs pull - подтянет все lfs файлы
```

## P.S. преимущества `git-lfs`

Предположим создаём файл объемом 100 МБ, изменяем его 100 раз. В итоге получим `.git` объемом 10 ГБ. `git-lfs` умным образом обработает изменения и будет удерживать размер репозитория в адекватных пределах