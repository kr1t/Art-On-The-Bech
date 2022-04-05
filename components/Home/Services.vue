<template>
<!-- service area start here -->
<section id="service" class="service-area pt-120 pb-130" :style="{backgroundImage: 'url('+require('../../public/assets/img/service/service-bg.jpg') +')'}">
    <div class="container">
        <div class="row justify-content-between">
            <div class="col-xl-5 col-lg-6">
                <div class="kservice-text mb-50" data-aos="fade-right" data-aos-duration="1000">
                    <h5 class="kservice-text-subtitle mb-15">{{ subtitle }}</h5>
                    <h2 class="kservice-text-title mb-40" v-html="title">{{ title }}</h2>
                    <p class="mb-45">{{ description }}</p>
                    <div class="kservice-author">
                        <div class="kservice-author-img mr-30">
                            <img :src="require('../../public/assets/img/service/' + authorImg)" class="img-fluid" alt="author-img">
                        </div>
                        <div class="kservice-author-sign">
                            <span>{{ authorName }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-xl-6 col-lg-6">
                <div class="row custom-mar-20" data-aos="fade-down" data-aos-duration="1000">
                    <div class="col-sm-6 custom-pad-20" v-for="item in serviceBox" :key="item.title">
                        <div class="kservice text-center mb-20">
                            <div class="kservice-icon">
                                <i><font-awesome-icon :icon="item.f_icon" /></i>
                            </div>
                            <div class="kservice-content">
                                <h5 class="kservice-content-title">
                                    <NuxtLink :to="item.url" v-html="item.serviceBoxTitle">{{ item.serviceBoxTitle }}</NuxtLink>
                                </h5>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<!-- service area end here -->
</template>

<script>
export default {
    name: 'Service',
    data() {
        return {
            subtitle: 'All Categories List',
            title: 'The Services <br>We’re Offering',
            description: 'Art on the Beach is just 200 metres to the sea with uninterupted views of the shoreline, situated on the Pae-Klaeng-kram Beach Road just 3 klms to Laem Mae Phim. Approximately 12 klms away is the Koh Samed ferry and rayong marriott resort & spa just 2klms.',
            authorImg: 'service-author.png',
            authorName: 'Art on the Beach',
            serviceBox: [{
                    serviceBoxTitle: 'Condominium near the sea.',
                    url: '/#',
                    // url: '/servicedetails',
                    f_icon: ['fas', 'swimming-pool'],
                },
                {
                    serviceBoxTitle: '180 degrees view of swimming pool',
                    url: '/#',
                    f_icon: ['fas', 'swimmer'],
                },
                {
                    serviceBoxTitle: 'Sky View Gymnasium',
                    url: '/#',
                    f_icon: ['fas', 'dumbbell']
                },
                {
                    serviceBoxTitle: 'Free WIFI',
                    url: '/#',
                    f_icon: ['fas', 'wifi']
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
