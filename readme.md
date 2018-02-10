# Используется CSSSR Project Template
**Тестовое задание для 1vds**
**Реализована авторизация (проверка имени пользователя и пароля, редирект в случае успеха). Добавление и удаление домена/БД. Комментарии в коде присутствуют**
**Рабочие файлы /app/scripts/app.js и /app/pages/ index и login**


## Старт проекта

### Склонируй репозиторий и перейди в папку проекта
```
git clone git@github.com:Georgeek/1vds-test.git new-project && cd new-project
```

### Установи модули

```
npm i
```

### Запусти шаблон
```
npm start
```


## Команды для запуска

### Запуск с отслеживанием изменений
```
npm start
```

### Сборка в папку `dist`
```
npm run build
```

### Production cборка в папку `dist`
```
npm run production
```

## Git hooks
Используется [husky](https://github.com/typicode/husky). Перед каждым `git push` запускается линтер.
Если линтер падает с ошибкой, `git push` не пройдет. Пропустить линтинг можно, используя `git push --no-verify`.


## Структура папок и файлов
```
├── app/                       # Исходники
│   ├── blocks/                # Блоки
│   │   └── block/             # Блок
│   │       ├── block.jade     # Разметка блока
│   │       ├── block.js       # Скрипт блока
│   │       └── block.styl     # Стили блока
│   ├── data/                  # Данные в формате JSON
│   ├── pages/                 # Страницы
│   │   └── index.jade         # Разметка страницы
│   ├── icons/                 # SVG иконки для генерации векторного спрайта
│   ├── sprites/               # PNG иконки для генерации растрового спрайта
│   ├── resources/             # Статические файлы для копирования в dist
│   ├── scripts/               # Скрипты
│   │   └── app.js             # Главный скрипт
│   └── styles/                # Стили
│       ├── helpers/           # Помощники
│       │   ├── fonts.styl     # Подключение шрифтов
│       │   ├── mixins.styl    # Примеси
│       │   ├── optimize.styl  # Сброс стилей и фиксы
│       │   ├── svg-size.styl  # Переменные с размерами SVG иконок (автосборка)
│       │   └── variables.styl # Переменные
│       ├── sprites/           # Переменные с данными PNG спрайтов (автосборка)
│       └── app.styl           # Главный стилевой файл
├── dist/                      # Сборка (автогенерация)
│   ├── assets/                # Подключаемые ресурсы
│   │   ├── fonts/             # Шрифты
│   │   ├── images/            # Изображения
│   │   │   └── sprites/       # Спрайты (автогенерация)
│   │   ├── scripts/           # Скрипты
│   │   └── styles/            # Стили
│   └── index.html             # Страница
├── tasks/                     # Подключаемые скрипты с задачами для gulpfile.babel.js
│   ├── copy.js                # Копирование
│   ├── default.js             # Итоговые списки задач по умолчанию
│   ├── deploy.js              # Деплой в ветку dist
│   ├── icons.js               # Сборка SVG иконок в один файл
│   ├── scripts.js             # Сборка ES2015 скриптов в Webpack
│   ├── semver.js              # Обновление версии шаблона
│   ├── server.js              # Запуск локального сервера
│   ├── sprite.js              # Сборка спрайтов и CSS переменных
│   ├── styles.js              # Сборка стилей
│   ├── templates.js           # Сборка страниц из Jade шаблонов
│   ├── watch.js               # Отслеживание изменений и запуск задач
│   └── zip.js                 # Архивация папки dist
├── .csscomb.json              # Конфигурация форматирования CSS
├── .eslintrc                  # Конфигурация проверки JavaScript в ESLint
├── .editorconfig              # Конфигурация настроек редактора кода
├── .gitignore                 # Список исключённых файлов из Git
├── browserlist                # Список версий браузеров для Autoprefixer
├── gulpfile.babel.js          # Файл для запуска Gulp.js
├── make-block.js              # Утилита создания новых блоков
├── package.json               # Список модулей и прочей информации
├── readme.md                  # Документация шаблона
└── webpack.conf.js            # Конфигурация Webpack.js
```
