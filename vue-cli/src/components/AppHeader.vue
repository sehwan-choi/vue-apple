<template>
  <header>
    <h1>{{ propsdata }}</h1>
    <button v-on:click="sendUpEvent">up</button>
    <button v-on:click="sendDownEvent">down</button>
    <input v-model="message" v-on:keypress="keyEvent">
  </header>
</template>

<script>
export default {
    props: ['propsdata'],
    data: function() {
        return {
            num: 10,
            message: ''
        }
    },
    methods: {
        sendUpEvent: function() {
            this.num++;
            this.$emit('renew', this.num);
        },
        sendDownEvent: function () {
            this.num--;
            this.$emit('renew', this.num);
        },
        keyEvent: function() {
            this.$emit('keyOn', this.message);
        }
    }
}
</script>

<style>

</style>