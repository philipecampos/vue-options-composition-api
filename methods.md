## Options API
```vue

<script>
  export default {
    methods: {
      printMessage() {
        return "my result"
      },
      printSpecificMessage(message) {
        return message
      },
    },
  }
</script>
```

## Compostion API

```vue

<script setup>
  const printMessage = () => {
    return "my result"
  };

  const printSpecificMessage = (message) => {
    return message
  };
</script>
```

## Template
```vue

<template>
  <div>
    <p>{{ printMessage() }}</p>
    <p>{{ printSpecificMessage("my result") }}</p>
  </div>
</template>
```