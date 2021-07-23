<template>
    <v-app :theme="theme">
        <v-main>
            <v-btn
                color="primary"
                text
                variant="outlined"
                size="x-small"
                @click="toggleTheme"
                >toggle theme</v-btn
            >
            <router-view />
        </v-main>
    </v-app>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'App',
    setup() {
        const theme = ref('light')
        return {
            theme,
            toggleTheme: () =>
                (theme.value = theme.value === 'light' ? 'dark' : 'light'),
        }
    },
})
</script>
