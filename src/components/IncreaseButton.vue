<template>
    <div>
        <button @click="plusOne">Increase!</button>
    </div>
</template>
<script>
export default {
    name: 'IncreaseButton',
    methods: {
        plusOne() {
            // emit an event to the counterResult
            // we don't have to specify second param here
            this.$emit('IncreaseOne')
        }
    }
}
</script>