<template>
<!-- cta area start here -->
<section class="cta-area mt--60 z-index" data-aos="fade-up">
    <div class="container">
        <div class="cta-bg bg-theme">
            <div class="cta-number">
                <div class="cta-number-icon mr-30">
                    <img :src="require('../../public/assets/img/icon/cta-icon.png')" class="img-fluid z-index" alt="about-img">
                </div>
                <div class="cta-number-text fix">
                    <span class="uppercase">{{ subtitle }}</span>
                    <h3><a href="tel:+66645563644">{{ numberText }}</a></h3>,
                    <h3><a href="tel:+6638638155">{{ numberText2 }}</a></h3>
                </div>
            </div>
            <div class="cta-description">
                <p v-html="description">{{ description }}</p>
            </div>
            <div class="cta-btn">
                <NuxtLink :to="ctaLinkUrl" class="theme-btn black-btn">{{ ctaLinkText }}</NuxtLink>
            </div>
        </div>
    </div>
</section>
<!-- cta area end here -->
</template>

<script>
export default {
    name: 'Cta',
    data(){
        return {
            subtitle: 'Get a Free Consultation',
            numberText: '(+66)64-556-3644',
            numberText2: '(+66)38-638-155',
            description: '298 Moo 2, Chakphong, Klaeng District, Rayong 21190<br>contact@artonthebeachrayong.com,<br>artonthebeachrayong@gmail.com',
            ctaLinkText: 'Discover more',
            ctaLinkUrl: '/service',
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
