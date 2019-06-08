<template>
    <div class="container">
        <div class="case-box">
            <i class="fas fa-briefcase fa-lg"></i>
        </div>
        <h2 class="title">sample <span class="works">works</span></h2>
        <p>Let’s take a look at some of the best of our works here, 
            we love them and hope you too</p>
        <div class="samples">
            <SampleBox 
                v-for="n in 8"
                :key="n"
                :title="samples.title"
                :info="samples.info"
                :likes="samples.likes"/>
        </div>
        <button class="view-all">view all works</button>
    </div>
</template>

<script>
import SampleBox from '@/components/SampleWorks/SampleBox';
export default {
    name: 'SampleWorks',
    components: {
        SampleBox,
    },
    data() {
        return {
            samples: {title: 'Corporate Brochure',
                    info: 'Illustration / Print',
                    likes: 22}
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
    width: 100%;
    background-color: #383838;
    text-align: center;
    color: #8A8A8A;
}

.case-box {
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

.case-box i {
    transform: rotate(-45deg);
}

.title {
    font-weight: bold;
    text-transform: uppercase;
    color: #ffffff;
    margin: 0;
}

.works {
    color: var(--main-color);
}

.samples {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
}

.view-all {
    width: 60%;
    height: 45px;
    margin: 50px 0 110px 0;
    text-transform: uppercase;
    background-color: var(--main-color);
    border: none;
    border-radius: 5px;
}

</style>
