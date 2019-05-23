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
