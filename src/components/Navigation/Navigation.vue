<template>
    <div class="container">
        <div class="top">
            <div class="logo">
                <img 
                src="@/assets/logo1.png" 
                id="logo"/>
                <h2>startapp</h2>
            </div>
            <Toolbar />
        </div>
        <div class="top-line"></div>
        <div class="bottom">
            <NavigationContent />
        </div>
    </div>
</template>

<script>
import Toolbar from '@/components/Navigation/Toolbar';
import NavigationContent from '@/components/Navigation/NavigationContent';

export default {
    name: 'Navigation',
    components: {
        Toolbar,
        NavigationContent,
    }

}
</script>

<style scoped>
.container {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: auto;
}
.top {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    height: auto;
}

.logo {
    display: flex;
    flex-direction: row;
    align-items: center;
    color: #A0A0A0;
}
.logo img {
    width: 40px;
    height: 40px;
}

.top-line {
    position: absolute;
    top: 70px;
    display: block;
    width: 100%;
    height: 2px;
    background-color: #DEDEDE;
}
.bottom {
    width: 60%;
    margin: 80px 0 0 0;
}

@media screen and (max-width: 1860px) {
    .top {
        flex-direction: column;
        width: 100%;
    }  
    .top-line {
        top: 130px;
    } 
}

@media screen and (max-width: 850px) { 
    .top-line {
        top: 420px;
    } 
}

</style>
