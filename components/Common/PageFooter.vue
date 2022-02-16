<template>
    <footer :style="{backgroundImage: 'url('+require('../../public/assets/img/bg/footer-bg.jpg') +')'}" class="pt-95 position-relative">
        <div class="common-shape-wrapper wow slideInRight animated" data-wow-delay="0ms" data-wow-duration="1500ms">
            <div class="common-shape-inner wow slideInRight animated" data-wow-delay="0ms" data-wow-duration="1500ms"></div>
        </div>
        <div class="footer-area pb-60">
            <div class="container">
                <div class="row">
                    <div class="col-lg-4 col-sm-6">
                        <div class="widget mb-30">
                            <div class="footer-logo mb-25">
                                <NuxtLink to="/"><img src="../../public/assets/img/logo/logo-white.png" class="img-fluid" alt="footer-logo"></NuxtLink>
                            </div>
                            <p class="mb-20 pr-35">
                              Condominium Near Beach
                              <br>180 Degree Roof Top Panoramic
                              <br>Swimming Pool
                              <br>Sky View Gymnasium</p>
                            <div class="footer-social">
                                <a href="#" target="_blank"><font-awesome-icon :icon="['fab', 'twitter']"/></a>
                                <a href="#" target="_blank"><font-awesome-icon :icon="['fab', 'facebook']"/></a>
                                <a href="#" target="_blank"><font-awesome-icon :icon="['fab', 'pinterest-p']"/></a>
                                <a href="#" target="_blank"><font-awesome-icon :icon="['fab', 'instagram']"/></a>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-2 col-sm-6">
                        <div class="widget mb-30">
                            <h4 class="widget-title mb-35">Links</h4>
                            <ul>
                                <li><NuxtLink to="/#">Our Services</NuxtLink></li>
                                <li><NuxtLink to="/#">Meet Our Team</NuxtLink></li>
                                <li><NuxtLink to="/#">Our Portfolio</NuxtLink></li>
                                <li><NuxtLink to="/#">Contact</NuxtLink></li>
                                <li><NuxtLink to="/#">Help</NuxtLink></li>
                                <!-- <li><NuxtLink to="/service">Our Services</NuxtLink></li>
                                <li><NuxtLink to="/about">Meet Our Team</NuxtLink></li>
                                <li><NuxtLink to="/project">Our Portfolio</NuxtLink></li>
                                <li><NuxtLink to="/contact">Contact</NuxtLink></li>
                                <li><NuxtLink to="/contact">Help</NuxtLink></li> -->
                            </ul>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6">
                        <div class="widget widget-contact mb-30">
                            <h4 class="widget-title mb-35">Contact</h4>
                            <ul>
                                <li class="pb-10">298 Moo 2, Chakphong, Klaeng District, Rayong 21190</li>
                                <li><img src="../../public/assets/img/icon/footer-icon-1.png" class="img-fluid" alt="icon-img"><a href="mailto:contact@artonthebeachrayong.com">contact@artonthebeachrayong.com</a></li>
                                <li><img src="../../public/assets/img/icon/footer-icon-1.png" class="img-fluid" alt="icon-img"><a href="mailto:artonthebeachrayong@gmail.com">artonthebeachrayong@gmail.com</a></li>
                                <li><img src="../../public/assets/img/icon/footer-icon-2.png" class="img-fluid" alt="icon-img"><a href="tel:+66645563644">(+66)64-556-3644</a></li>
                                <li><img src="../../public/assets/img/icon/footer-icon-2.png" class="img-fluid" alt="icon-img"><a href="tel:+6638638155">(+66)38-638-155</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6">
                        <div class="widget mb-30">
                            <h4 class="widget-title mb-30">Newsletter</h4>
                            <p class="mb-20">Subscribe to Our Newsletter for Daily News and Updates</p>
                            <div class="widget-newsletter">
                                <form action="#">
                                    <input type="email" placeholder="Email Address">
                                    <button type="submit">Send</button>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="copyright-area" style="background-color: #1a1c1e;">
           <div class="container">
                <div class="copyright-bg">
                    <div class="row align-items-center">
                        <div class="col-md-6">
                            <div class="copyright">
                                <span>Copyright ©2021 Art On The Beach. All Rights Reserved</span>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="privacy-text text-center text-md-end">
                                <ul>
                                    <li>
                                        <NuxtLink to="/#">Terms & Condition</NuxtLink>
                                        <NuxtLink to="/#">Privacy Policy</NuxtLink>
                                        <!-- <NuxtLink to="/contact">Terms & Condition</NuxtLink>
                                        <NuxtLink to="/contact">Privacy Policy</NuxtLink> -->
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'PageFooter'

}
</script>

<style lang="scss" scoped>

</style>











