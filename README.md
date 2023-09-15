# Задание 3

Необходимо реализовать верстку и js-логику одного компонента-спойлера  
При клике на спойлер он переключается между открытым и закрытым состоянием  
Внутри спойлера может быть произвольное количество текста  
В открытом состоянии всё содержимое спойлера должно отображаться не обрезая текст

[Ссылка на макет](https://www.figma.com/file/Dnpu2tvo6fyDEDtFcySkfa/%D0%A1%D1%82%D0%B0%D0%B6%D0%B8%D1%80%D0%BE%D0%B2%D0%BA%D0%B0---%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-3?type=design&node-id=0%3A1&mode=design&t=ogE3qWw0Gddljan0-1)  
**Срок выполнения: 1 неделя**

> Дополнительно:
> 
> Реализовать [анимацию](https://drive.google.com/file/d/1fDVGNnp19Ud3q-0z708Tsgx9QYvJDxNh/view?usp=sharing) плавного открытия/закрытия спойлеров 

## Работа с компонентами

### Создание компонента

Для генерации pug, scss, js файлов компонента необходимо ввести команду:
```shell
npm run component:create [название-компонента]
```
**[название-компонента]** - произвольное название компонента, записанное латиницей  

Например:
```shell
npm run component:create example-button
```
Таким образом в папке `src/components` будет создана папка `example-button` с готовыми для работы pug, scss, js файлами внутри.  
Все созданные файлы будут добавлены в сборщик автоматически

> Для инициализации js-скриптов компонентов необходимо вручную добавить импорт в файл `/src/app/js/common.js` и добавить созданный компонент в объект `allComponents`

### Удаление компонента
Для удаления существующего компонента необходимо ввести команду:
```shell
npm run component:remove [название-компонента]
```
**[название-компонента]** - произвольное название компонента, записанное латиницей

Например:
```shell
npm run component:remove example-button
```
Таким образом в папке `src/components` будет удалена папка `example-button`  
Все pug, scss файлы, относящиеся к компоненту будут удалены из сборщика автоматически

## Работа с проектом

### Требования к системе
- Node.js (v.16+)
- npm (v.7+)

### Запуск проекта
1) Установить зависимости
    ```shell
    npm i
    ```
2) Запустить локальную dev-сборку
    ```shell
    npm run dev
    ```
    Запущенный локальный сервер будет доступен в браузере по адресу [localhost:3000](http://localhost:3000/)

### Краткое описание файловой структуры
```
/
├── build_modules
└── src
    ├── app
    │   ├── js
    │   │   └── base
    │   └── common.js
    ├── assets
    │   ├── fonts
    │   ├── icons
    │   ├── images
    │   └── videos
    ├── components
    └── pages
```
- `build_modules` - служебная директория, необходимая для сборки и запуска проекта. **В рамках задания изменять содержимое папки нельзя**
- `src` - основная рабочая директория, содержащая исходный код проекта
- `src/app` - директория, содержащая основные файлы приложения
- `src/app/js` - директория, содержащая основную логику приложения
- `src/app/common.js` - основной js-файл, точка входа для всех скриптов приложения
- `src/app/base` - директория для хранения базовых js-классов
- `src/assets` - необязательная директория для хранения статичных ресурсов (шрифты, изображения, видео, иконки)
- `src/components` - директория для хранения исходного кода компонентов. Каждый компонент располагается в отдельной папке и может состоять из pug, scss и ts файлов
- `src/pages` - директория для хранения статичных страниц
