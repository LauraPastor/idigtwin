<template>
    <Header />
    <MainSection />
    <Footer />
</template>

<script>
import Header from './Header.vue';
import MainSection from './MainSection.vue';
import Footer from './Footer.vue';

export default {
    name: 'Home',
    components: {
        Header,
        MainSection,
        Footer
    }
}
</script>
