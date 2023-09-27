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

You can choose using the ```ref()``` or ```reactive()``` function to create a reactive variable.
Using ```ref()``` you **need** to use ```.value``` to access the value, using ```reactive()``` you don't need to
use ```.value``` to access the value.

```vue

<script setup>
  import {ref, reactive} from "vue"

  const counter = ref(0),
      counterTitle = ref("Counter")

  const myVariables = reactive({
    counter: 0,
    title: "Counter"
  })

  const increment = () => {
    counter.value++
    myVariables.counter++
  }
</script>
```

## Template

It's the same for all sintaxes

```vue

<template>
  <div>
    <p>{{ counterTitle }}: {{ counter }}</p>
    <p>{{ myVariables.title }}: {{ myVariables.counter }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>
```