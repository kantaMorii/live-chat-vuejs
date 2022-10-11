<template>
    <div>
        <h1>{{ title }}</h1>
        <TestComponent />
    </div>
</template>

<script>
import TestComponent from '@/components/TestComponent.vue'
export default {
    data() {
        return {
            title: "初めてのVue.jsアプリです！",
            subtitle: "ようこそ",
            isEnabled: true
        };
    },
    computed: {
        text() {
            if (this.isEnabled) {
                return "こんにちは！";
            }
            else {
                return "さよなら！";
            }
        }
    },
    methods: {
        toggle() {
            this.isEnabled = !this.isEnabled;
        }
    },
    components: { TestComponent }
}
</script>