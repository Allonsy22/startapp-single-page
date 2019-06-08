<template>
    <div class="container">
        <div class="top">
            <div class="key-box">
                <i class="fas fa-key fa-lg"></i>
            </div>
            <div class="features-content-container">
                <h2 class="title">amazing <span class="features">features</span></h2>
                <p>With unlimited features that we offer, we promise it’s possible
                    to make everything that was imposible for you!
                </p>
                <div class="content">
                    <div class="left-content">
                        <div 
                            v-for="(leftCard, i) in leftCards"
                            :key="i"
                            class="card-container">
                                <i 
                                    style="color: #00A99D"
                                    :class="leftCard.icon"></i>
                                <div class="card-description">
                                    <p class="card-title">{{leftCard.title}}</p>
                                    <p class="card-text">{{leftCard.text}}</p>
                                </div>
                        </div>
                    </div>
                    <div class="right-content">
                        <img src="@/assets/tablets.png" />
                    </div>
                </div>
            </div>
        </div>
        <div class="bottom">
            <div class="cards">
                <FeaturesCard 
                v-for="(card, i) in cards"
                :key="i"
                :icon="card.icon"
                :title="card.title"
                :text="card.text"
                :info="card.info"/>
            </div>
        </div>
    </div>
</template>

<script>
import FeaturesCard from '@/components/Features/FeaturesCard';

export default {
    name: 'Features',
    components: {
        FeaturesCard,
    },
    data() {
        return {
            leftCards: [
                {title: 'responsive & multipurpose',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                icon: 'fas fa-tv fa-2x'},
                {title: 'easy customization',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                icon: 'fas fa-puzzle-piece fa-2x'},
                {title: 'unlimited features',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                icon: 'fas fa-star fa-2x'},
            ],
            cards: [
                {title: 'responsive & multipurpose',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `Desktops, Tablets & Phones`,
                icon: 'fas fa-tv fa-lg'},
                {title: 'easy customization',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `One Click Demo Content Installation`,
                icon: 'fas fa-puzzle-piece fa-lg'},
                {title: 'unlimited features',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `Shortcodes, Typography & Different Layouts`,
                icon: 'fas fa-star fa-lg'},
                {title: 'clean & modular coding',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `100% Clean, Valid & Well-Commented Coding`,
                icon: 'fas fa-list fa-lg'},
                {title: 'the best e-commerce solutions',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `WooCommerce Fully Integration`,
                icon: 'fas fa-shopping-cart fa-lg'},
                {title: 'awesome friendly support',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit.`,
                info: `Free Lifetime Support & Updates`,
                icon: 'fas fa-user-friends fa-lg'},
            ]
        }
    }
}
</script>

<style scoped>
.container {
    position: relative;
    width: 100%;
    display: flex;
    flex-direction: column;
}

.top {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #383838;
}

.key-box {
    position: relative;
    top: -27px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 55px;
    height: 55px;
    border-radius: 5px;
    transform: rotate(45deg);
    background-color: var(--main-color);
    color: #ffffff;
}

.features-content-container {
    width: 60%;
    text-align: center;
    color: #5D5D5D;
}

.title {
    color: #ffffff;
    text-align: center;
    text-transform: uppercase;
}

.features {
    color: var(--main-color);
}

.content {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 100%;
}

.left-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 35%;
}

.card-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}

.card-description {
    display: flex;
    flex-direction: column;
    margin-left: 20px;
}

.right-content {
    position: relative;
    bottom: -4px;
    width: 50%;
}

.right-content img{
    max-width: 100%;
    height: auto;
}

.card-title {
    margin: 0;
    text-transform: uppercase;
    color: #ffffff;
}

.card-text {
    margin: 10px 0;
    font-size: 14px;
}

.bottom {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.cards {
    width: 60%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 30px 0 0 0;
}

@media screen and (max-width: 1200px){
    .content {
        flex-direction: column-reverse;
    }
}
</style>
