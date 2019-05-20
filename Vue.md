# Vue

### Bind Events

```html
<button @click="increase(2, $event)">...</button>
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
