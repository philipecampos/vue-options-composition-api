## Options api

```vue

<script>
  export default {
    data() {
      return {
        counter: 0,
        counterTitle: "Counter",
      };
    },
    methods: {
      increment() {
        this.counter++
      },
    },
  };
</script>
```

## Composition API (old version)

```vue

<script>
  import {ref} from "vue"

  export default {
    setup() {
      const counter = ref(0),
            counterTitle = ref("Counter")

      const increment = () => {
        counter.value++
      }

      return {
        counter,
        increment
      }
    }
  }
</script>
```

## Composition API (new version)

```vue

<script setup>
  import {ref} from "vue"

  const counter = ref(0),
        counterTitle = ref("Counter")
  
  const increment = () => {
    counter.value++
  }
</script>
```

## Template

It's the same for all sintaxes

```vue

<template>
  <div>
    <p>{{ counterTitle }}: {{ counter }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>
```