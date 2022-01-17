<template>
<!-- blog area start here -->
<section class="blog-area pt-120" :style="{backgroundImage: 'url('+require('../../public/assets/img/blog/blog-bg-1.jpg') +')'}">
    <div class="blog-space pb-120">
        <div class="blog-text pt-60" data-aos="zoom-in">
            <div class="section-title-wrapper pr-25 mb-50">
                <h5 class="section-subtitle mb-20">{{ sectionSubTitle }}</h5>
                <h2 class="section-title mb-35">{{ sectionTitle }}</h2>
                <p class="pr-50">{{ sectionTitleDescription }}</p>
            </div>
            <!-- If we need navigation buttons -->
            <div class="kblog-arrow">
                <div class="blog-button-prev slide-prev">
                    <font-awesome-icon :icon="['fas', 'long-arrow-alt-left']" />
                </div>
                <div class="blog-button-next slide-next">
                    <font-awesome-icon :icon="['fas', 'long-arrow-alt-right']" />
                </div>
            </div>
        </div>
        <div class="blog-active swiper-container">
            <div class="swiper-wrapper">
                <client-only>
                    <swiper ref="mySwiper" class="swiper" :options="swiperOptions" @ready="onSwiperRedied"  @clickSlide="onSwiperClickSlide">
                        <swiper-slide v-for="item in blogs" :key="item.id">
                            <div class="kblog swiper-slide">
                                <div class="kblog-img">
                                    <NuxtLink :to="item.imageUrl"><img :src="require('../../public/assets/img/blog/' + item.image)" class="img-fluid" alt="blog-img"></NuxtLink>
                                    <!-- <span>{{ item.date }}</span> -->
                                </div>
                                <div class="kblog-text">
                                    <!-- <div class="kblog-meta">
                                        <NuxtLink :to="item.metaAdminUrl">
                                            <font-awesome-icon :icon="['far', 'user-circle']" />{{ item.metaAdmin }}</NuxtLink>
                                        <NuxtLink :to="item.metaCommentUrl">
                                            <font-awesome-icon :icon="['far', 'comments']" />{{ item.metaComment }}</NuxtLink>
                                    </div> -->
                                    <h3 class="kblog-text-title mb-20">
                                        <NuxtLink :to="item.titleUrl"> {{ item.title}}</NuxtLink>
                                    </h3>
                                    <div class="kblog-text-link">
                                        <NuxtLink :to="item.blogLinkUrl">{{ item.blogLink }}
                                            <font-awesome-icon :icon="['fas', 'chevron-right']" />
                                        </NuxtLink>
                                    </div>
                                </div>
                            </div>
                        </swiper-slide>
                    </swiper>
                </client-only>
            </div>
        </div>
    </div>
</section>
<!-- blog area end here -->
</template>

<script>

export default {
    name: 'swiper-slider3',
    data() {
        return {
            sectionSubTitle: 'recent rooms',
            sectionTitle: 'ROOM TYPE',
            sectionTitleDescription: '”Art on the Beach condo” has 4 types of room. Type A, Type B, Type C and Suite room.',
            blogs: [{
                    id: '1',
                    image: 'room/typeA.jpg',
                    imageUrl: '/blogdetails',
                    date: '20 May',
                    metaAdmin: 'by Admin',
                    metaAdminUrl: '/blogdetails',
                    metaComment: '2 Comments',
                    metaCommentUrl: '/blogdetails',
                    title: 'Type A',
                    titleUrl: '/blogdetails',
                    blogLink: 'Read more',
                    blogLinkUrl: '/blogdetails',
                },
                {
                    id: '2',
                    image: 'room/typeB.jpg',
                    imageUrl: '/blogdetails',
                    date: '21 May',
                    metaAdmin: 'by Admin',
                    metaAdminUrl: '/blogdetails',
                    metaComment: '2 Comments',
                    metaCommentUrl: '/blogdetails',
                    title: 'Type B',
                    titleUrl: '/blogdetails',
                    blogLink: 'Read more',
                    blogLinkUrl: '/blogdetails',
                },
                {
                    id: '3',
                    image: 'room/typeC.jpg',
                    imageUrl: '/blogdetails',
                    date: '22 May',
                    metaAdmin: 'by Admin',
                    metaAdminUrl: '/blogdetails',
                    metaComment: '2 Comments',
                    metaCommentUrl: '/blogdetails',
                    title: 'Type C',
                    titleUrl: '/blogdetails',
                    blogLink: 'Read more',
                    blogLinkUrl: '/blogdetails',
                },
                {
                    id: '4',
                    image: 'room/typeSuite.jpg',
                    imageUrl: '/blogdetails',
                    date: '23 May',
                    metaAdmin: 'by Admin',
                    metaAdminUrl: '/blogdetails',
                    metaComment: '2 Comments',
                    metaCommentUrl: '/blogdetails',
                    title: 'Suite room',
                    titleUrl: '/blogdetails',
                    blogLink: 'Read more',
                    blogLinkUrl: '/blogdetails',
                },
                // {
                //     id: '5',
                //     image: 'blog-img-5.jpg',
                //     imageUrl: '/blogdetails',
                //     date: '24 May',
                //     metaAdmin: 'by Admin',
                //     metaAdminUrl: '/blogdetails',
                //     metaComment: '2 Comments',
                //     metaCommentUrl: '/blogdetails',
                //     title: 'We work with change oriented executives',
                //     titleUrl: '/blogdetails',
                //     blogLink: 'Read more',
                //     blogLinkUrl: '/blogdetails',
                // }
            ],
            swiperOptions: {
                slidesPerView: 1,
                spaceBetween: 30,
                loop: false,
                infinite: false,
                autoplay: {
                    delay: 5000,
                },
                pagination: {
                    el: '.swiper-pagination',
                    clickable: true,
                    dynamicBullets: false,
                },
                navigation: {
                    nextEl: '.blog-button-next',
                    prevEl: '.blog-button-prev',
                },
                breakpoints: {
                    480: {
                        slidesPerView: 1,
                    },
                    576: {
                        slidesPerView: 2,
                    },
                    768: {
                        slidesPerView: 2,
                    },
                    1200: {
                        slidesPerView: 2,
                    },
                    1400: {
                        slidesPerView: 3,
                    },
                }
            }
        }
    },
    methods: {
      onSwiperRedied(swiper) {
        console.log('Swiper redied!', swiper)
      },
      onSwiperClickSlide(index, reallyIndex) {
        console.log('Swiper click slide!', reallyIndex)
      }
    }
}
</script>

<style lang="scss" scoped>

</style>
