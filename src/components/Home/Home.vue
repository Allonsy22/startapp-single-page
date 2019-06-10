<template>
    <div class="header">
        <div class="title-block">
            <p>What are you waiting for?</p>
            <h1>Let's be creative!</h1>
            <div class="motivation-block">
                <span class="double-line"></span>
                <p><span class="start">Start</span> Doing that</p>
                <span class="double-line"></span>
            </div>
            <div class="down">
                <a href="#logo" aria-label="Navigation"><i class="fas fa-chevron-down fa-2x"></i></a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Home',
}
</script>

<style scoped>
.header {
    width: 100%;
    height: 100vh;
    display: flex;
    background-color: gray;
}

.title-block {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    text-transform: uppercase;
    margin: 225px 0 0 20%;
    color: #383838;
}

.title-block h1 {
    font-size: 3em;
    font-weight: bold;
    margin: 0;
}

.title-block p {
    margin: 0 0 3px 0;
}

.motivation-block {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin: 50px 0;
    justify-content: center;
    align-items: center;
    font-size: 18px;
    font-weight: bold;
}

.double-line {
    width: 120px;
    height: 6px;
    border-top: 2px solid #ffffff;
    border-bottom: 2px solid #ffffff;
}

.start {
    color: #00A99D;
}

.down {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    border: 4px solid #00A99D;
    color: #00A99D;
    cursor: pointer;
    animation: down 2s 1;
}

@keyframes down {
    50% {
        color: #60F6F6;
        border: 4px solid #60F6F6;
    }
    100% {
        border: 4px solid #00A99D;
        color: #00A99D;
    }
}

@media screen and (max-width: 1360px) {
    .header {
        justify-content: center;
        align-items: center;
    }
    .title-block {
        margin: 0;
    }
}
</style>
