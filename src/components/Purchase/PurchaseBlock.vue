<template>
    <div class="container">
        <div class="content">
            <h3>are you satisfied with unlimited features that we offer?</h3>
            <button class="btn">purchase it now</button>
            <button class="btn">contact us now</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PurchaseBlock',
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-color: var(--main-color);
}

.content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    color: #ffffff;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
}

.btn {
    width: 150px;
    height: 40px;
    margin: 5px;
    background-color: #E2E2E2;
    border: none;
    border-radius: 5px;
    font-size: 12px;
    text-transform: uppercase;
}

@media screen and (max-width: 1200px) {
    .content {
        flex-direction: column;
    }
}
</style>
