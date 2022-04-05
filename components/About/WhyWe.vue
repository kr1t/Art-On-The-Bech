<template>
<section class="why-we bg-grey pt-125 pb-75 position-relative fix">
    <div class="common-shape-wrapper wow slideInLeft animated" data-wow-delay="0ms" data-wow-duration="1500ms">
        <div class="common-shape-inner"></div>
    </div>
    <div class="container z-index">
        <div class="row justify-content-between">
            <div class="col-xl-6 col-lg-6 col-md-12">
                <div class="choose-left mb-40 mr-xs-0 mr-md-0 mr-lg-0 mr-90" data-aos="fade-up-right" data-aos-duration="1000">
                    <div class="section-title-wrapper">
                        <h5 class="section-subtitle mb-20">{{ sectionSubTitle }}</h5>
                        <h2 class="section-title mb-35">{{ sectionTitle }}</h2>
                    </div>
                    <p>{{ sectionTitleContent }}</p>
                    <div class="why-tab-list">
                        <ul>
                            <li v-for="item in whyTabList" :key="item.List"><i>
                                    <font-awesome-icon :icon="['fas', 'check']" /></i> {{ item.List }}</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="col-xl-6 col-lg-6 col-md-12">
                <div class="faq-wrapper">
                    <div class="choose-right" data-aos="fade-left" data-aos-duration="1000">
                        <div class="accordion" role="tablist">
                            <b-card no-body>
                                <b-card-header header-tag="header" role="tab">
                                    <b-button block v-b-toggle.accordion-1 variant="info">{{ tabTitle1 }}</b-button>
                                </b-card-header>
                                <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                                    <b-card-body>
                                        <b-card-text>{{ Text1 }}</b-card-text>
                                    </b-card-body>
                                </b-collapse>
                            </b-card>

                            <b-card no-body>
                                <b-card-header header-tag="header" role="tab">
                                    <b-button block v-b-toggle.accordion-2 variant="info">{{ tabTitle2 }}</b-button>
                                </b-card-header>
                                <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                                    <b-card-body>
                                        <b-card-text>{{ Text2 }}</b-card-text>
                                    </b-card-body>
                                </b-collapse>
                            </b-card>

                            <b-card no-body>
                                <b-card-header header-tag="header" role="tab">
                                    <b-button block v-b-toggle.accordion-3 variant="info">{{ tabTitle3 }}</b-button>
                                </b-card-header>
                                <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                                    <b-card-body>
                                        <b-card-text>{{ Text3 }}</b-card-text>
                                    </b-card-body>
                                </b-collapse>
                            </b-card>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
</template>

<script>
export default {
    data() {
        return {
            sectionSubTitle: 'All of we',
            sectionTitle: 'Why Choose We',
            sectionTitleContent: 'The accommodation provides excellent facilities. These include hiking, private beach, fitness room, outdoor pool. Guests can relax after a long drive.',

            whyTabList: [{
                    List: 'Condominium near the sea.',
                },
                {
                    List: '180 degrees view of swimming pool.',
                },
                {
                    List: 'Sky View Gymnasium.',
                }
            ],
            tabTitle1: 'Art on the beach residential condominium was built in 2017',
            tabTitle2: 'This double unit condo has been tailor-made',
            tabTitle3: 'A unique balcony bar has been fitted to enjoy the tranquil views with a pool and Gym on the roof.',

            Text1: 'Located all on its own on the beach road just 5 klm from the main popular area of this small beach town.',
            Text2: 'with open plan solid teak wood flooring and a king size bath which is on the 6th floor overlooking the sea and nothing else but trees either side.',
            Text3: 'It offers night security, reception, Wifi and covered parking.European kitchen, 2 aircon units, 2 balconies  NOTE : Solid matching wood furniture throughout not included in the sale price, but is available and recommended as an option to purchase for an additional TB 250,000.',
        };
    },
};
</script>

<style lang="scss" scoped>

</style>
