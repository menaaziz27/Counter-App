<template>
    <div>
        <button @click="minusOne">Decrease!</button>
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
            this.$emit('increaseOne');
        },

        minusOne() {
            this.$emit('decreaseOne');
        }
    }
}
</script>