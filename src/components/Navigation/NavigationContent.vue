<template>
    <div class="container">
        <div class="offer-block">
            <div class="line"></div>
            <h2 class="title">what we <span class="offer">offer</span></h2>
            <div class="line"></div>
        </div>
        <p>We offer our customers the best services &amp; solutions, this is o</p>
        <div class="cards">
            <NavigationCard 
                v-for="(card, i) in cards"
                :key="i"
                :icon="card.icon"
                :text="card.text"
                :title="card.title"/>
        </div>
    </div>
</template>

<script>
import NavigationCard from '@/components/Navigation/NavigationCard';

export default {
    name: 'NavigationContent',
    components: {
        NavigationCard,
    },
    data() {
        return {
            cards: [
                {title: 'responsive &amp; multipurpose',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit. Consequuntur autem 
                        facere corporis dolores molestias hic 
                        recusandae eos similique! Tenetur quia 
                        quae, illo ut eum natus obcaecati modi 
                        alias nisi cum?`,
                icon: 'fas fa-tv fa-2x'},
                {title: 'easy customization',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit. Consequuntur autem 
                        facere corporis dolores molestias hic 
                        recusandae eos similique! Tenetur quia 
                        quae, illo ut eum natus obcaecati modi 
                        alias nisi cum?`,
                icon: 'fas fa-puzzle-piece fa-2x'},
                {title: 'awesome friendly support',
                text: `Lorem ipsum dolor sit amet consectetur 
                        adipisicing elit. Consequuntur autem 
                        facere corporis dolores molestias hic 
                        recusandae eos similique! Tenetur quia 
                        quae, illo ut eum natus obcaecati modi 
                        alias nisi cum?`,
                icon: 'fas fa-user-friends fa-2x'},
            ]
        }
    }
}
</script>

<style scoped>
.container {
    width: 100%;
    height: auto;
    text-align: center;
}

.offer-block {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    font-size: 18px;
    text-transform: uppercase;
    font-weight: bold;
}

.title {
    text-align: center;
    text-transform: uppercase;
}

.offer {
    color: #06AB9F;
}

.line {
    width: 35%;
    height: 5px;
    border: none;
    border-top: 1px solid #000000;
    border-bottom: 1px solid #000000;
}

.cards {
    display: flex;
    flex-direction: row;
    margin: 50px 0 100px 0;
}

@media screen and (max-width: 850px) {
    .cards {
        flex-direction: column;
    }
}
</style>
