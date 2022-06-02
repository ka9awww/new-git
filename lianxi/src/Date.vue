<template>
 <button @click="$emit('handleChange','2022-05-30')">2022-05-30</button>
 <button @click="$emit('handleChange','2022-05-31')">2022-05-31</button>
</template>

<script>
export default {
    emits: {
        dateChange(payload) {
            return typeof payload === 'string'
        },
    },
    methods: {
        handleChange(date) {
            this.$emit('dateChange',date)
        }
    }
}
</script>