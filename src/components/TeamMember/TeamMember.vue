<template>
    <div class="container">
        <div class="title">
            <div class="line"></div>
            <h2><span class="team">Team</span> members</h2>
            <div class="line"></div>
        </div>
        <p class="title-info">We’re some creative people with powerful knowledge &amp; awesome sk</p>
        <div class="cards">
            <TeamCard 
                v-for="n in 4"
                :key="n"
                :name="members.name"
                :specialization="members.specialization"
                :email="members.email"
                :phone="members.phone"/>
        </div>
    </div>
</template>

<script>
import TeamCard from '@/components/TeamMember/TeamCard';

export default {
    name: 'TeamMember',
    components: {
        TeamCard,
    },
    data() {
        return {
            members: {name: "Alexander Hendr", specialization: "User Interface Designer",
                    email: "Email@email.com", phone: "222 (22) 222 2222"}
        }
    }
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.title {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    margin: 80px 0 0 0;
    text-transform: uppercase;
    text-align: center;
}

.title-info {
    margin: 0;
}

.team {
    color: var(--main-color);
}

.line {
    display: block;
    width: 35%;
    height: 5px;
    border-top: 2px solid #DEDEDE;
    border-bottom: 2px solid #DEDEDE;
}

.cards {
    display: flex;
    flex-wrap: wrap;
    width: 60%;
    align-items: center;
    justify-content: space-around;
    margin: 60px 0;
}

@media screen and (max-width: 500px) {
    .cards {
        width: 100%;
    }
}
</style>
