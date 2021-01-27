<template>
    <div>
        <button @click="minusOne">Decrease!</button>
    </div>
</template>


<script>
export default {
    name: 'DeacreaseButton',
    methods: {
        minusOne() {
            this.$emit("decreaseOne");
        }
    }
}
</script>