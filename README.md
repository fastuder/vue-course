# Notizen - Vue Kurs

**CDN:** `<script src="https://unpkg.com/vue@next"></script>`

## Table Of Contents

- [Interpolation und Data Binding](#Interpolation-und-Data-Binding)
- [Binding Attributes](#Binding-Attributes)
- [Methoden und Event Binding](#Methoden-und-Event-Binding)

## Ressources

### Vue.js

- [Class Component Syntax](https://class-component.vuejs.org/)
- [Vue.js 3](https://v3.vuejs.org/guide/introduction.html)
- [Vue.js 2](https://vuejs.org/v2/guide/)
- [Vue.js Udemy Kurs](https://www.udemy.com/course/vuejs-2-the-complete-guide/)

### Typescript

- [TS for Javascript Devs](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
- [Typescript - The Basics](https://www.youtube.com/watch?v=ahCwqrYpIuM)

## Grundkonzepte

### Interpolation und Data Binding

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Boilerplate</title>

    <script src="https://unpkg.com/vue@next" defer></script>
  </head>
  <body>
    <div id="app">
      <!-- Data Binding and Interpolation -->
      <h2>{{ message }}</h2>
    </div>
  </body>
</html>
```

```js
const app = Vue.createApp({
  data() {
    return {
      // Data Binding and Interpolation
      message: "hello world",
    };
  },
});
app.mount("#app");
```

### Binding Attributes

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Boilerplate</title>

    <script src="https://unpkg.com/vue@next" defer></script>
  </head>
  <body>
    <div id="app">
      <!-- Binding Attribute with v-bind Directive -->
      <a :href="myLink">My Github</a>
    </div>
  </body>
</html>
```

```js
const app = Vue.createApp({
  data() {
    return {
      // Attribute
      myLink: "https://github.com/lianstuder",
    };
  },
});
app.mount("#app");
```

### Methoden und Event-Binding

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Boilerplate</title>

    <script src="https://unpkg.com/vue@next" defer></script>
  </head>
  <body>
    <div id="app">
      <button v-on:click="outputMessage">Click me</button>
      <p>{{ outputMessage() }}</p>
    </div>
  </body>
</html>
```

```js
const app = Vue.createApp({
  data() {
    return {};
  },
  methods: {
    outputMessage() {
      const randomNum = Math.random();
      if (randomNum < 0.5) return "Hello world";
      return "Bye world";
    },
  },
});
app.mount("#app");
```

[Zurück nach oben](#Table-Of-Contents)
