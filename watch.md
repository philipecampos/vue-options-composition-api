## Options API

```vue

<script>
  export default {
    data() {
      return {
        counter: 0,
        form: {
          name: "",
        },
      };
    },
    watch: {
      counter(newValue, oldValue) {
        console.log(newValue, oldValue);
      },
      'form.name'(newValue, oldValue) {
        console.log(newValue, oldValue);
      },
    },
  }
</script>
```

## Compostion API

```vue

<script setup>
  const counter = ref(0)
  const form = reactive({
    name: "",
  });

  watch(counter, (newValue, oldValue) => {
    console.log(newValue, oldValue);
  });

  watch(() => form.name, (newValue, oldValue) => {
    console.log(newValue, oldValue);
  });
</script>
```