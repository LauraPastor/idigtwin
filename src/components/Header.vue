<template>
    <header>
        <nav class="navbar">
            <div class="container">
                <div class="navbar-header">
                    <Logo :isLink="true" />
                    <h1>Industrial Digital Twin</h1>
                </div>
                <div class="" id="">
                    <ul class="nav-items">
                        <li class="nav-item">
                            <router-link class="nav-link" to="/">Home</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link class="nav-link" to="/about">About</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link class="nav-link" to="/contact">Contact</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>
<script>
import Logo from './Logo.vue';
export default {
    name: 'Header',
    components: {
        Logo,
    },
}
</script>

<style scoped>
header {
    background-color: #f8f9fa;
    padding: 15px 0;
    border-bottom: 1px solid #dee2e6;
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

}

.navbar-header {
    display: flex;
    align-items: center;
}

.navbar {
    padding-left: 0;
}


.nav-link {
    color: #6c757d;
    font-weight: bold;
}

.nav-link:hover {
    color: #007bff;
    text-decoration: none;
}
</style>
