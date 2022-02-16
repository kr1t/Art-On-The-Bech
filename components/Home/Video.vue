<template>
<!-- video area start here -->
<section class="video-area z-index">
    <div class="container">
        <div class="row">
            <div class="col-12">
                <div class="section-title-wrapper mb-45 text-center">
                    <h5 class="section-subtitle mb-20">{{ sectionSubTitle }}</h5>
                    <h2 class="section-title mb-35">{{ sectionTitle }}</h2>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-lg-12">
                <div class="kvideo-wrapper" data-aos="zoom-in" data-aos-duration="1000">
                    <div class="kvideo" :style="{backgroundImage: 'url('+require('../../public/assets/img/bg/video-bg.jpg') +')'}">
                        <div class="kvideo-sign text-center">
                            <b-button v-b-modal.modal-center>
                                <font-awesome-icon :icon="['fas', 'play']" />
                            </b-button>
                            <h2>{{ watchTitle }}</h2>
                        </div>
                        <div class="kvideo-number">
                            <span>{{ numTitle }}</span>
                            <a href="tel:+66645563644">{{ number }},</a>
                            <a href="tel:+6638638155">{{ number2 }}</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div>

        <!-- vue bootstrap modal -->
        <div class="video-modal-wrapper">
            <b-modal id="modal-center" centered title="BootstrapVue">
                <p><video-embed src="https://www.youtube.com/watch?v=u5kcYLqrxnA"></video-embed></p>
            </b-modal>
        </div>
        <!-- vue bootstrap modal -->
    </div>
</section>
<!-- video area end here -->
</template>

<script>
export default {
    name: 'Video',
    data() {
        return {
            sectionSubTitle: 'one minute video',
            sectionTitle: 'Watch video work',
            watchTitle: 'Watch Video',
            numTitle: 'get estimate',
            number: '(+66)64-556-3644',
            number2: '(+66)38-638-155',
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
