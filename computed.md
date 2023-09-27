## Options Api

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

## Compostion Api

```html

<script setup>
    import {computed} from "vue"

    const myComputedProperty = computed(() => {
        return "my result"
    });
</script>
```
