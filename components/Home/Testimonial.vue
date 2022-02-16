<template>
<!-- testimonial area start here -->
<section class="testimonial-area pt-115 pb-85">
    <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <div class="section-title-wrapper text-center mb-45">
                    <h5 class="section-subtitle mb-20">{{ sectionSubTitle }}</h5>
                    <h2 class="section-title mb-35">{{ sectionTitle }}</h2>
                </div>
            </div>
        </div>

        <div class="testimonial-active">
            <client-only>
                <swiper ref="mySwiper" class="swiper" :options="swiperOptions" @ready="onSwiperRedied"  @clickSlide="onSwiperClickSlide">
                    <swiper-slide v-for="item in testimonialContent" :key="item.id">
                        <div class="ktestimonial mb-30 swiper-slide">
                            <div class="ktestimonial-text">
                                <p>{{ item.description }}</p>
                            </div>
                            <div class="ktestimonial-author">
                                <div class="ktestimonial-author-img">
                                    <img :src="require('../../public/assets/img/testimonial/' + item.image)" class="img-fluid" alt="client_img">
                                </div>
                                <div class="ktestimonial-author-text">
                                    <h5 class="uppercase">{{ item.clientName }}</h5>
                                    <span class="uppercase">{{ item.clientStatus }}</span>
                                </div>
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>
            </client-only>
        </div>
    </div>
</section>
<!-- testimonial area end here -->
</template>

<script>

export default {
    name: 'swiper-slider6',
    data() {
        return {
            sectionSubTitle: 'client testimonials',
            sectionTitle: 'What they say?',
            testimonialContent: [{
                    id: '1',
                    image: 'testimonial-img-1.jpg',
                    description: `I decided to buy one unit here without any hesitation for a  family holiday  because I love the location. The nice sea breeze  with beautiful beach and ocean overlooking armostphere where I can have all here at Art on the Beach Codo. It's awesome! And more importantly, it is worth and best  for my future investment.`,
                    clientName: `MR.FRANK SMITH`,
                    clientStatus: `The owner of room number 298/60. 7th. Floor.`,
                },
                {
                    id: '2',
                    image: 'testimonial-img-2.jpg',
                    description: `A price that everyone can afford , Design and decoration, In the heart of Mae Phim Beach, Comfortable travel, Nice view, good atmosphere, Location near the sea`,
                    clientName: `MISS.LALITA JAMSAI`,
                    clientStatus: `The owner of room number 298/35. 4th. Floor.`,
                },
                {
                    id: '3',
                    image: 'testimonial-img-3.jpg',
                    description: `I decided to buy one unit here without any hesitation for a  family holiday  because I love the location. The nice sea breeze  with beautiful beach and ocean overlooking armostphere where I can have all here at Art on the Beach Codo. It's awesome! And more importantly, it is worth and best  for my future investment.`,
                    clientName: `MR.FRANK SMITH`,
                    clientStatus: `The owner of room number 298/60. 7th. Floor.`,
                },
                {
                    id: '4',
                    image: 'testimonial-img-4.jpg',
                    description: `A price that everyone can afford , Design and decoration, In the heart of Mae Phim Beach, Comfortable travel, Nice view, good atmosphere, Location near the sea`,
                    clientName: `MISS.LALITA JAMSAI`,
                    clientStatus: `The owner of room number 298/35. 4th. Floor.`,
                },
            ],
            swiperOptions: {
                slidesPerView: 1,
                spaceBetween: 30,
                loop: true,
                infinite: false,
                centeredSlides: true,
                autoplay: {
                    delay: 5000,
                },
                pagination: {
                    el: '.swiper-pagination',
                    dynamicBullets: false
                },
                breakpoints: {
                    480: {
                        slidesPerView: 1,
                    },
                    768: {
                        slidesPerView: 2,
                    },
                    1200: {
                        slidesPerView: 3,
                    },
                    1400: {
                        slidesPerView: 3,
                    }
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
