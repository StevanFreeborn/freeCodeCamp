---
id: 587d7fb6367417b2b2512c06
title: Встановлення і налаштування Mongoose
challengeType: 2
forumTopicId: 301540
dashedName: install-and-set-up-mongoose
---

# --description--

Робота над цими завданнями включатиме написання вашого коду з використанням одного з наступних методів:

- Клонуйте <a href="https://github.com/freeCodeCamp/boilerplate-mongomongoose/" target="_blank" rel="noopener noreferrer nofollow">цей репозиторій GitHub</a> та виконайте ці завдання локально.
- Використайте <a href="https://replit.com/github/freeCodeCamp/boilerplate-mongomongoose" target="_blank" rel="noopener noreferrer nofollow">наш стартовий проєкт Replit</a> для виконання цих завдань.
- Використовуйте конструктор сайту на власний розсуд, щоб завершити проєкт. Перевірте, що ви зберегли усі файли з нашого репозиторію GitHub.

По завершенню, переконайтеся, що працююча демоверсія вашого проєкту розміщена у відкритому доступі. Потім введіть URL - адресу проєкту в поле `Solution Link` field.

У цьому завданні, створіть базу даних MongoDB Atlas та імпортуйте необхідні пакети для підключення до неї.

Follow <a href='https://www.freecodecamp.org/news/get-started-with-mongodb-atlas/' target="_blank" rel="noopener noreferrer nofollow">this tutorial</a> to set up a hosted database on MongoDB Atlas.

# --instructions--

`mongoose@^5.11.15` has been added to your project’s `package.json` file. First, require mongoose as `mongoose` in `myApp.js`. Next, create a `.env` file and add a `MONGO_URI` variable to it. Його значенням має бути ваш URI бази даних MongoDB Atlas. Обов'язково помістіть URI в одинарні чи подвійні лапки, і пам'ятайте, що ви не можете використовувати пробіли навколо `=` у змінних середовища. Наприклад, `MONGO_URI='VALUE'`.

**Note:** If you are using Replit, you cannot create a `.env` file. Instead, use the built-in <dfn>SECRETS</dfn> tab to add the variable. <em>Do not</em> surround the values with quotes when using the <em>SECRETS</em> tab.

When you are done, connect to the database using the following syntax:

```js
mongoose.connect(<Your URI>, { useNewUrlParser: true, useUnifiedTopology: true });
```

# --hints--

"mongoose version ^5.11.15" dependency should be in package.json

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/file/package.json').then(
    (data) => {
      var packJson = JSON.parse(data);
      assert.property(packJson.dependencies, 'mongoose');
      assert.match(
        packJson.dependencies.mongoose,
        /^\^5\.11\.15/,
        'Wrong version of "mongoose". It should be ^5.11.15'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

"mongoose" should be connected to a database

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/is-mongoose-ok').then(
    (data) => {
      assert.isTrue(data.isMongooseOk, 'mongoose is not connected');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--

```js
/**
  Backend challenges don't need solutions, 
  because they would need to be tested against a full working project. 
  Please check our contributing guidelines to learn more.
*/
```
