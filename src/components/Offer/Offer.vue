<template>
    <div class="container">
        <h2 class="title">real cheap <span class="prices">prices</span></h2>
        <p>We offer all our services in real low prices in comparison with</p>
        <div class="cards">
            <OfferCard 
                v-for="n in 4"
                :key="n"
                :plan="cards.plan"
                :price="cards.price"
                :offers="cards.offers"/>
        </div>
    </div>
</template>

<script>
import OfferCard from '@/components/Offer/OfferCard';

export default {
    name: 'Offer',
    components: {
        OfferCard,
    },
    data() {
        return {
            cards: {
                price: 22, 
                offers: ["10 Projects", "15 GB Storage", "Unlimited Users", "20 GB Bandwith"],
                plan: "Standart Plan"
            }
        }
    }
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-items: center;
    width: 100%;
    text-align: center;
}

.title {
    font-weight: bold;
    text-transform: uppercase;
    margin: 85px 0 0 0;
}

.prices {
    color: var(--main-color);
}

.cards {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    width: 60%;
    margin: 75px 0;
}
</style>
