<template>
    <nav class="toolbar">
        <ul class="toolbar-container">
            <li><a href="#home">home</a></li>
            <li><a href="#portfolio">portfolio</a></li>
            <li><a href="#blog">blog</a></li>
            <li><a href="#pages">pages</a></li>
            <li><a href="#features">features</a></li>
            <li><a href="#megaMenu">mega menu</a></li>
            <li><a href="#contact">contact</a></li>
            <li><input 
                id="search" 
                type="text" 
                class="search"
                placeholder="search"/></li>
            <li><i 
                class="fas fa-search fa-lg"
                @click="activateSearch"></i></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Toolbar',
    methods: {
        activateSearch() {
            let searchInput = document.getElementById('search');
            searchInput.classList.toggle('active-search');
        },
        showMenu() {
            let toolbar = document.querySelector(".toolbar-container");
            toolbar.classList.toggle('active-menu');
        }
    }
}
</script>

<style scoped>
.toolbar {
    display: flex;
    flex-direction: row;
}
.toolbar-container {
    list-style-type: none;
    margin: 0;
    padding: 0;
    float: left;
}
.toolbar-container li {
    display: inline-block;
}

.toolbar-container li a{
    display: inline-block;
    font-size: 16px;
    font-weight: bold;
    text-transform: uppercase;
    text-decoration: none;
    text-align: center;
    line-height: 40px;
    padding: 0 10px;
    height: 40px;
    border-radius: 5px;
    color: #606060;
}

.toolbar-container li a:hover {
    background-color: #00A99D;
    color: #ffffff;
}

.search {
    display: block;
    width: 0;
    height: 40px;
    margin-right: 15px;
    border: none;
    border-bottom: 2px solid #00A99D;
    font-size: 16px;
    color: #00A99D;
    transition: width .5s ease-in;
}

.active-search {
    width: 150px;
}

@media screen and (max-width: 850px) {
    .toolbar-container li {
        display: block;
    }
    .search {
        width: 150px;
    }
    .toolbar-container i {
        display: none;
    }
}
</style>
