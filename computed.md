## Options API

```html

<script>
    export default {
        computed: {
            myComputedProperty() {
                return "my result"
            },
        },
    };
</script>
```

## Compostion API

```html

<script setup>
    import {computed} from "vue"

    const myComputedProperty = computed(() => {
        return "my result"
    });
</script>
```
