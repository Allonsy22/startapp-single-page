<template>
    <div class="container">
        <div class="icon-container">
            <i :class="icon"></i>
        </div>
        <p class="title">{{title}}</p>
        <p>{{text}}</p>
        <button class="read-more">read more</button>
    </div>
</template>

<script>
export default {
    name: 'NavigationCard',
    props: {
        icon: String,
        title: String,
        text: String,
    },
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 20px 0;
    text-align: center;
    color: #8A8A8A;
}

.icon-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: #383838;
    color: #ffffff;
}

.title {
    text-transform: uppercase;
    font-weight: bold;
}

.read-more {
    width: 100px;
    height: 30px;
    background-color: transparent;
    border: 1px solid #F1F1F1;
    border-radius: 5px;
    text-transform: uppercase;
}

.read-more:hover {
    background-color: #00A99D;
    color: #ffffff;
}
</style>
