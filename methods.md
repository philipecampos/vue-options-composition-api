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

```vue
<template>
    <div>
        <p>{{ printMessage() }}</p>
        <p>{{ printSpecificMessage("my result") }}</p>
    </div>
</template>
```