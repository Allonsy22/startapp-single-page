<template>
    <div class="sample-container">
        <div class="more">
            <h3>{{title}}</h3>
            <p>{{info}}</p>
            <div class="likes">
                <i class="fas fa-heart"></i>
                {{likes}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SampleBox',
    props: {
        title: String,
        info: String,
        likes: Number,
    }
}
</script>

<style scoped>
.sample-container {
    width: 320px;
    height: 250px;
    margin: 5px;
    background-color: #8A8A8A;
    text-align: center;
    color: #ffffff;
}

.more {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    opacity: 0;
    background-color: var(--main-color);
    cursor: pointer;
    transition: opacity .5s linear;
}

.more:hover {
    opacity: 1;
}
</style>
