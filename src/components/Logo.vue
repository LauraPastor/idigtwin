<template>
    <div>
        <router-link v-if="isLink" to="/">
            <img class="logo" alt="Vue logo" src="../assets/home.jpg">
        </router-link>
        <img v-else class="logo" alt="Vue logo" src="../assets/home.jpg">
    </div>
</template>
<script>
export default {
    name: 'Logo',
    props: {
        isLink: {
            type: Boolean,
            default: false,
        }
    }
}
</script>