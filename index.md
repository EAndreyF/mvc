---

layout: default

---

# Яндекс

## **{{ site.presentation.title }}** {#cover}

{% if site.presentation.nda %}
<div class="nda"></div>
{% endif %}

<div class="info">
	<p class="author">{{ site.author.name }}, <br/> {{ site.author.position }}</p>
</div>

## &nbsp;
{:.section}

### Разминка

## Какие есть типы в JS?

* ...Number
* ...String
* ...Boolean
* ...Undefined
* ...Null
* ...Object
* ...Symbol

## Что возвращает typeof?

* Number → <span>...number</span>
* String → <span>...string</span>
* Boolean → <span>...boolean</span>
* Undefined → <span>...undefined</span>
* Null → <span>...object</span>
* Symbol → <span>...symbol</span>
* Object → <span>...object</span>
* ...Function → <span>...function</span>

## Как проверить тип переменной `t`?

* Number, String, Boolean → <span>...`typeof t`</span>
* ...undefined, null → <span>...`t === undefined, null`</span>
* ...Массив → <span>...`Array.isArray(t)`</span>
* ...Объект → <span>...`typeof t`</span><span>...`, Object(t) === t`</span>

## Что будет в консоли?

~~~javascript
var i = 10;
var array = [];

while (i--) {
    array.push(function() {
        return i + i;
    });
}

console.log([
     array[0](),
     array[1](),
])
~~~

...[-2, -2]

## Как вывести `yandex` вызвав функцию `fn`

~~~javascript
var obj = {x: 'yandex'}
function fn() { console.log(this.x); }
~~~

...fn.call(obj);

...fn.apply(obj);

...fn.bind(obj)();

## Зачем нужны паттерны?

* ...Не нужны для маленького приложения
* ...Эффективно решать однотипные проблемы
* ...Для быстрого понимания кода


## &nbsp;
{:.section}

### MVC

## Состав компонент
![placeholder](pictures/mvc.png){:.right-image}

* Model
* View
* Клей (Controller, Presenter, Router)

## &nbsp;
{:.section}

### Клиент-серверный MVC

## Серверный рендеринг

* ...Только сервер генерит html
* ...Быстрая шаблонизация и кэширование
* ...Отсутствие динамики
* ...Актуальная серверная модель
* ...Сокрытие бизнес-логики

![](pictures/server-mvc.png)

// Примеры сайтов с серверным рендерингом

## Клиентский рендеринг

* ...Долгая первоначальная отрисовка страницы
* ...Не рабочий сайт при отключенном JS
* ...Интерактивность
* ...Открытая бизнес-логика
* ...Синхронизация модели

![](pictures/client-mvc.png)

## Клиент-серверный рендеринг

* ...Быстрая первоначальная загрузка
* ...Работает при отключении JS
* ...Интерктивность
* ...Сокрытие нужной части бизнес-логики
* ...Синхронизация модели

![](pictures/client-server-mvc.png)

// Нравится последний подход, говорить будем только про MVC на клиенте

## Домашнее задание

* Написать собственный MVC
* Написать TodoMVC

![](pictures/todomvc.png)

## Клиентский MVC
{:.section}

### View (представление)

## Что такое представление?

* HTML
* Биндинги
* Состояние
* Перерисовка

## Задача

* Отрендерить шаблон / подвязаться к html
* Обновление представления новыми данными
* Подписка на пользовательские события

## Анализ альтернатив

* ...Низкая или высокая интерактивность
* ...Сервер поставляет разметку или данные
* ...Первичность модели или разметки (чтение из DOM)
* ...Гранулярность обновления (представление, элемент, строка)
* ...CSS или собственные селекторы биндингов

## Клиентский MVC
{:.section}

### Model

## Состав
![](pictures/model-detail.png)

## Задача

* ...Хранить состояние приложения
* ...Получать / обновлять состояние на сервере
* ...Не допускать дублирования сущностей
* ...Генерировать событие при изменении (альтернативы?)
* ...Изменение вложенных моделей


## Клиентский MVC
{:.section}

### Controller

## Задача

* ...Роутинг приложения
* ...Стейт приложения (онлайн, офлайн)
* ...Связь модели и представления

## Клиентский MVC
{:.section}

### Альтернативы

## MVC, MVP, MVVM
![](pictures/mv.png)

[MV*](https://addyosmani.com/blog/understanding-mvc-and-mvp-for-javascript-and-backbone-developers/)

## &nbsp;
{:.section}

### Собственный MVC

## С чего начать

* ...Модульность → <span>...CommonJS модули + browserify</span>
* ...Событийная модель → <span>...EventEmitter + listenTo</span>
* ...Шаблонизация → <span>...ES6 шаблоны</span>
* ...Работа с API → <span>...абстракция над LocalStorage</span>
* ...Клиентский роутинг → <span>...historyAPI</span>
* ...Выделение компонентов и определение ответственности

[SPA](http://singlepageappbook.com/)
<i>Без части implementing</i>

[TodoMVC](http://todomvc.com/)

[TodoMVC template](https://github.com/hse2016/todomvc-app-template)

## &nbsp;
{:.section}

### Вопросы?
