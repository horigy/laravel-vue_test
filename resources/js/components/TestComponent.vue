<template>
    <div class="container">
        <h1>Hello, Laravel!</h1>
        <h2>Меня зовут</h2>
        <div class="user">
            <div class="user-data">
                <span>{{user.name}}</span>
                <span>{{user.surname}}</span>
            </div>
            <div class="user-pic">
                <img v-bind:src="user.imgUrl" alt="">
            </div>
        </div>



    </div>
</template>

<script>
export default {
    data() {
        return {
            user: {
                name: 'Nikolay',
                surname: 'Gerasimov',
                imgUrl: 'https://media.licdn.cn/dms/image/C5103AQE-2B69yAgJ4w/profile-displayphoto-shrink_400_400/0/1517550089699?e=1628121600&v=beta&t=hs9Fwa9bpwjdCbW8w1fFdAQEusAHi_qYFq6syyzmcBY'
            },
        }
    },
}
</script>

<style lang="scss" scoped>
.container {
    display: flex;
    align-items: center;
    flex-direction: column;
    margin: 10% 0;
}
.user {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 60px;
}
.user-pic > img {
    border-radius: 50%;
}
</style>
