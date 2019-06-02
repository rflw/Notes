# Vue

### Bind Events

- `$event` - access to DOM event
- `@click` - `v-on:click` shorthand, it could be also `@keydown, @<nameEvent>`

```html
<button @click="increase(2, $event)">...</button>
```

Modify component value

```html
new Vue({
  el: '#loremIpsum',
  data: {
    value: ''
  },
  methods: {
    modifyValue(event) {
      this.value = event.target.value;
    }
  }
});

// inline (1)
<input type="text" v-on:keydown="value = $event.target.value">

// method (2)
<input type="text" @keydown="modifyValue">
```

### Event Modifiers

```html
// mousemove(event) {event.stopPropagation())
<span @mousemove.stop="">...</span>
```

### Key Modifiers

```html
// starts the `alert` function after pressing the enter key
<input type="text" @keyup.enter="alert">
```

### Two way data binding

```html
<input type="text" v-model="message" placeholder="edit me">
<p>Message is: {{ message }}</p>
```

### v-if vs v-show

- `v-if`:
  - detach/attach DOM element
  - can be used with `<template>`
  
- `v-show`:
  - only toggles `display` property (element is always rendered)
  - doesn't have `else`
  - can't be used with `<template>`

### Rendering lists (v-for) and getting index

```html
<ul>
  <li v-for="(item, index) in items">
    {{ index }} - {{ item.message }}
  </li>
</ul>

<!-- template'll generate not nested divs -->
<template v-for="(item, index) in items">
  <div>{{ index }} - {{ item.message }}</div>
</template>
```

```js
data: {
  items: [
    { message: 'Foo' },
    { message: 'Bar' }
  ]
}
```
