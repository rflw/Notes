# Vue

### Bind Events

```html
<button @click="increase(2, $event)">...</button>
```

### Access to DOM event

```html
<button v-on:click="warn('Form cannot be submitted yet.', $event)">
  Submit
</button>
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
