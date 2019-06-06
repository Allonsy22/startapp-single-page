<template>
    <div class="cards-container">
        <div class="icon">
            <img src="@/assets/cardIcon.png" />
            <i :class="icon"></i>
        </div>
        <div class="card-content">
            <p class="card-title">{{title}}</p>
            <p class="card-info">{{info}}</p>
            <p class="card-text">{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FeaturesCard',
    props: {
        title: String,
        info: String,
        text: String,
        icon: String,
    }
}
</script>

<style scoped>
.cards-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 250px;
    margin: 30px 0;
}

.icon {
    display: flex;
    align-items: center;
    justify-content: center;
    color: #ffffff;
}

.icon i {
    position: relative;
    top: -10px;
    left: -32px;
}

.card-title {
    text-transform: uppercase;
    font-weight: bold;
    margin: 0;
}

.card-info {
    margin: 0;
    font-size: 14px;
    color: #8B8B8B;
}

.card-content {
    display: flex;
    flex-direction: column;
}
</style>
