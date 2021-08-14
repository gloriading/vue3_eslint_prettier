<template>
    <hello-world />
</template>

<script>
import { defineComponent } from 'vue'
import HelloWorld from '../components/HelloWorld.vue'

export default defineComponent({
    name: 'Home',

    components: {
        HelloWorld,
    },

    // setup() {},
})
</script>
