<template>
    <div class="card-container">
        <div class="plan">{{plan}}</div>
        <div class="price">
            <i class="fas fa-dollar-sign"></i>
            <span class="integer">{{price}}.</span>
            <span class="decimal">99</span>
            <span>Monthly</span>
        </div>
        <div class="line"></div>
        <div class="offer">
            <p
                v-for="(offer, i) in offers"
                :key="i">{{offer}}</p>
        </div>
        <div class="line"></div>
        <button class="btn">sign up now</button>
    </div>
</template>

<script>
export default {
    name: 'OfferCard',
    props: {
        price: Number,
        plan: String,
        offers: Array,
    }
}
</script>

<style scoped>
.card-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 270px;
    height: 440px;
    margin: 15px 10px;
    border: 1px solid #DEDEDE;
}

.plan {
    position: relative;
    top: -20px;
    height: 40px;
    line-height: 40px;
    font-weight: bold;
    text-transform: uppercase;
    border-radius: 5px;
    padding: 0 10px;
    background-color: #383838;
    color: #ffffff;
    cursor: pointer;
}

.plan:hover {
    background-color: var(--main-color);
}

.price {
    margin: 0 0 30px 0;
}
.integer {
    font-size: 3.5em;
    font-weight: bold;
}

.decimal {
    position: relative;
    top: -30px;
    left: -10px;
}

.line {
    display: block;
    width: 90%;
    height: 1px;
    background-color: #DEDEDE;
}

.btn {
    width: 120px;
    height: 40px;
    margin: 30px 0;
    background-color: var(--main-color);
    border: none;
    border-radius: 5px;
    text-transform: uppercase;
    color: #ffffff;
    cursor: pointer;
}
</style>
