## Options api
```html

<script>
    export default {
        data() {
            return {
                contador: 0,
            };
        },
        methods: {
            incrementar() {
                this.contador++
            },
        },
    };
</script>
```

## Composition API (versão antiga)
```html
<script>
  import { ref } from "vue"
  
  export default {
    setup() {
      const contador = ref(0)

      const incrementar = () => {
        contador.value++
      }

      return {
        contador,
        incrementar
      }
    }
  }
</script>
```

## Composition API (versão nova)
```html
<script setup>
  import { ref } from "vue"
  
  const contador = ref(0)  
  const incrementar = () => {
    contador.value++
  }
</script>
```