<template>
    <footer class="container">
        <div class="purchase-container">
            <div class="purchase-content">
                <h2>UNIQUE! We Do <span class="heart"><i class="fas fa-heart"></i></span> It And Hope You Too</h2>
                <button class="purchase-btn">Purchase it now<i class="fas fa-shopping-cart"></i></button>
            </div>
        </div>
        <div class="contacts-container">
            <div class="logo">
                <img src="@/assets/logo1.png" alt="logo"/>
                <h2>startapp</h2>
            </div>
            <div class="contacts">
                <i class="fab fa-facebook-f fa-lg icon"></i>
                <i class="fab fa-twitter fa-lg icon"></i>
                <i class="fab fa-pinterest-p fa-lg icon"></i>
                <i class="fab fa-youtube fa-lg icon"></i>
                <i class="fab fa-linkedin-in fa-lg icon"></i>
                <i class="fab fa-google fa-lg icon"></i>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.purchase-container {
    display: flex;
    justify-content: center; 
    width: 100%;
    background-color: #8A8A8A;
}

.purchase-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    margin: 40px 0;
}
.heart {
    color: var(--main-color);
}

.purchase-btn {
    width: 185px;
    height: 45px;
    background-color: var(--main-color);
    border-radius: 5px;
    border: none;
    text-transform: uppercase;
    color: #ffffff;
}

.purchase-btn i {
    margin: 0 10px 0 20px;
}

.contacts-container {
    width: 100%;
    background-color: #383838;
}

.logo {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 60px 0;
    color: #A0A0A0;
}

.contacts {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 0 80px 0;
}

.icon {
    width: 50px;
    height: 50px;
    margin: 15px;
    border: 1px solid #606060;
    border-radius: 5px;
    line-height: 50px;
    text-align: center;
    color: #ffffff;
    cursor: pointer;
}

.icon:hover {
    background-color: var(--main-color);
}

@media screen and (max-width: 1200px) {
    .purchase-content {
        flex-direction: column;
    }
}

@media screen and (max-width: 500px) {
    .contacts {
        flex-direction: column;
    }
}
</style>
