<template>
    <div class="container">
        <h2>Кто вы?</h2>
        <div class="new-user">
            <label>Имя</label>
            <input v-model="newUser.name" type="text">
            <label>Фамилия</label>
            <input v-model="newUser.surname" type="text">
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            newUser: {
                type: Object,
                requred: true
            }
        },
        methods: {
            refreshUser() {
                this.$emit('newUser', this.newUser)
            }
        }
    }
</script>
