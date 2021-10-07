<template>
    <div class="main-container">
        <Header />
        <Wrapper />
        <Footer />
    </div>
</template>

<script>
import Header from '@/components/Header'
import Wrapper from '@/components/Wrapper'
import Footer from '@/components/Footer'
export default {
    name: 'App',
    components: {
        Header,
        Wrapper,
        Footer
    }
}
</script>
