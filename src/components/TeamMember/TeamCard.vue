<template>
    <div class="card-container">
        <div class="card-top">
            <div class="icons">
                <a href="#" class="icon">
                    <i class="fab fa-facebook-f"></i>
                </a>
                <a href="#" class="icon">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="#" class="icon">
                    <i class="fab fa-google"></i>
                </a>
            </div>
        </div>
        <div class="card-bottom">
            <div class="name">{{name}}</div>
            <p class="specialization">{{specialization}}</p>
            
            <div class="contacts">
                <i class="far fa-envelope"></i>
                {{email}}
            </div>
            <div class="contacts">
                <i class="fas fa-phone"></i>
                {{phone}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TeamCard',
    props: {
        name: String,
        specialization: String,
        email: String,
        phone: String,
    }
}
</script>

<style scoped>
.card-container {
    display: flex;
    flex-direction: column;
    width: 270px;
    height: 410px;
    margin: 5px;
    border: 1px solid #DEDEDE;
}

.card-top {
    display: block;
    height: 270px;
    background-color: #8A8A8A;
}

.icons {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    background-color: var(--main-color);
    opacity: 0;
    transition: opacity .5s linear;
}

.icons:hover {
    opacity: 1;
}
.icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 30px;
    height: 30px;
    border-radius: 5px;
    background-color: #ffffff;
    text-decoration: none;
    color: var(--main-color);
    transform: rotate(45deg);
}

.icon:hover {
    background-color: #383838;
    color: #ffffff;
}

.icon i {
    transform: rotate(-45deg);
}

.card-bottom {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.name {
    position: relative;
    top: -20px;
    height: 40px;
    padding: 0 20px;
    text-align: center;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 12px;
    color: #ffffff;
    line-height: 40px;
    border-radius: 5px;
    background-color: var(--main-color);
}

.specialization {
    margin: 0;
    text-transform: capitalize;
    border-bottom: 2px solid #EBEBEB;
}

.contacts {
    margin: 10px 0;
    color: #AAAAAA;
}
</style>
