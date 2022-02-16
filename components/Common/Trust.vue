<template>
<!-- trust area start here -->
<section class="trust-area pt-105 pb-120">
    <div class="trust-bg" :style="{backgroundImage: 'url('+require('../../public/assets/img/trust/trust-bg.jpg') +')'}"></div>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <div class="ktrust text-center z-index">
                    <h2 class="ktrust-title mb-45 wow fadeInUp" data-wow-delay=".2s" v-html="title">{{ title }}</h2>
                    <div class="ktrust-btn">
                        <NuxtLink :to="url" class="theme-btn">{{ buttonText }}</NuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<!-- trust area end here -->
</template>

<script>
export default {
    name: 'trust',
    data() {
        return {
            title: 'for experience better well-being',
            buttonText: 'Discover more',
            url: '/#',
            // url: '/service',
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
