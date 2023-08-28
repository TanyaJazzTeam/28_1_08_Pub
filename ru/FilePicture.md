Первый заголовок | Второй заголовок
--- | ---
Ячейка содержимого | Ячейка содержимого
Ячейка содержимого | Ячейка содержимого

Первый заголовок | Второй заголовок
--- | ---
Ячейка содержимого | Ячейка содержимого
Ячейка содержимого | Ячейка содержимого

![Цитадель](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Выравнивание по левому краю | По центру | Выровнено по правому краю
:-- | :-: | --:
столбец 3 | какой-то многословный текст | **1600 долларов США**
столбец 2 | центрированный | 12 долларов США
полоски зебры | аккуратны | ~~$1~~

Dillinger is a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor.

- Type some Markdown on the left
- См. HTML справа.
- Magic

# истинный

- Импортируйте HTML-файл и наблюдайте, как он волшебным образом преобразуется в Markdown.
- Перетаскивайте изображения (требуется связь с вашей учетной записью Dropbox)

Вы также можете:

- Импортируйте и сохраняйте файлы из GitHub, Dropbox, Google Drive и One Drive.
- Перетащите файлы уценки и HTML в Dillinger.
- Export documents as Markdown, HTML and PDF

Markdown — это легкий язык разметки, основанный на соглашениях о форматировании, которые люди обычно используют в электронной почте. Как пишет [Джон Грубер] на [сайте Markdown][df1]

> The overriding design goal for Markdown's formatting syntax is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it's been marked up with tags or formatting instructions.

Этот текст, который вы видите здесь, *на самом деле* написан в Markdown! Чтобы понять синтаксис Markdown, введите текст в левое окно и посмотрите результаты в правом.

### ЛОЖЬ

Для правильной работы Диллинджер использует ряд проектов с открытым исходным кодом:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] — потрясающий текстовый веб-редактор
- [markdown-it] — парсер Markdown работает правильно. Быстро и легко расширяется.
- [Twitter Bootstrap] — отличный шаблон пользовательского интерфейса для современных веб-приложений.
- [node.js] — событийный ввод-вывод для бэкэнда
- [Express] — быстрая платформа сетевых приложений node.js [@tjholowaychuk]
- [Gulp] — потоковая система сборки
- [Брейк-данс](https://breakdance.github.io/breakdance/) — конвертер HTML в Markdown
- [jQuery] - да

И, конечно же, сам Dillinger имеет открытый исходный код и имеет [публичный репозиторий][dill] на GitHub.

### Installation

![Илос](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Для работы Диллинджера требуется [Node.js](https://nodejs.org/) v4+.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Для производственных сред...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Плагины

В настоящее время Dillinger дополнен следующими плагинами. Инструкции по их использованию в вашем собственном приложении приведены ниже.

Плагин | ПРОЧТИ МЕНЯ
--- | ---
Дропбокс | [плагины/dropbox/README.md][PlDb]
GitHub | [плагины/github/README.md][PlGh]
Гугл Диск | [plugins/googledrive/README.md][PlGd]
Один диск | [plugins/onedrive/README.md][PlOd]
Середина | [plugins/medium/README.md][PlMe]
Гугл Аналитика | [plugins/googleanalytics/README.md][PlGa]

### Разработка

Хотите внести свой вклад? Большой!

Диллинджер использует Gulp + Webpack для быстрой разработки. Внесите изменения в свой файл и мгновенно увидите свои обновления!

Откройте свой любимый терминал и выполните эти команды.

Первая вкладка:

```sh
$ node app
```

Вторая вкладка:

```sh
$ gulp watch
```

(необязательно) Третье:

```sh
$ karma test
```

#### Здание для источника

Для производственного выпуска:

```sh
$ gulp build --prod
```

Создание готовых zip-архивов для распространения:

```sh
$ gulp build dist --prod
```

### Докер

Dillinger очень легко установить и развернуть в контейнере Docker.

По умолчанию Docker предоставляет порт 8080, поэтому при необходимости измените его в файле Dockerfile. Когда все будет готово, просто используйте Dockerfile для создания образа.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Это создаст образ Диллинджера и подключит необходимые зависимости. Обязательно замените `${package.json.version}` актуальной версией Dillinger.

После этого запустите образ Docker и сопоставьте порт с любым желаемым портом на своем хосте. В этом примере мы просто сопоставляем порт 8000 хоста с портом 8080 Docker (или любым другим портом, указанным в Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Проверьте развертывание, перейдя по адресу вашего сервера в предпочитаемом вами браузере.

```sh
127.0.0.1:8000
```

#### Кубернетес + Google Cloud

См. [KUBERNETES.md.](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Тодос
