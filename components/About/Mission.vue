<template>
  <section class="mission-area pt-120 fix">
    <div class="container">
      <div class="row">
        <div class="col-xl-6 col-lg-6">
          <div
            class="kintro-text mr-xs-0 mr-md-0 mr-lg-0 mr-70 mb-30"
            data-aos="fade-left"
            data-aos-duration="1000"
          >
            <div class="section-title-wrapper mb-25">
              <h5 class="section-subtitle mb-20">{{ sectionSubTitle }}</h5>
              <h2 class="section-title mb-35">{{ sectionTitle }}</h2>
              <p>{{ sectionContent }}</p>
            </div>
            <p class="mb-45">{{ sectionContent2 }}</p>
          </div>
        </div>
        <div class="col-xl-6 col-lg-6">
          <div
            class="kintro-img mb-30"
            data-aos="fade-right"
            data-aos-duration="1000"
          >
            <img
              :src="require('../../public/assets/img/about/' + image)"
              class="img-fluid"
              alt="about-img"
            />
            <div class="mission-img-text">
              <!-- <h4>{{imageTitle}}</h4> -->
              <!-- <NuxtLink :to="imageBtnUrl">{{ imageBtn }}</NuxtLink> -->
            </div>
          </div>
          <div class="ktrust-btn">
            <a href="#sectionInstallmentCal" class="theme-btn border-btn" >{{
              buttonText
            }}</a>
          </div>
        </div>
      </div>

      <div class="detailContent">
        <h2 class="my-5">Details of the condominium project - promotion</h2>
        <div class="dContent">
          <div class="dTitle">Project name :</div>
          <div class="dDesc">Art On The Beach</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Project owner :</div>
          <div class="dDesc">Innovation House 2012</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Price :</div>
          <div class="dDesc">1,700,000 baht (as of launch date)</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Average price per sq m. :</div>
          <div class="dDesc">Please inquire with the project.</div>
        </div>

        <div class="dContent">
          <div class="dTitle">Installment Calculator :</div>
          <div class="dDesc">
            Swimming pool, fitness, security guard, CCTV project, Key Card door,
            garden
          </div>
        </div>

        <div class="dContent">
          <div class="dTitle">Location :</div>
          <div class="dDesc">Beachfront condo</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Condo height :</div>
          <div class="dDesc">Low Rise (up to 8 floors)</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Proprietary nature :</div>
          <div class="dDesc">Ownership</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Available room types :</div>
          <div class="dDesc">Please inquire with the project.</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Available room size :</div>
          <div class="dDesc">From 29.00 to 74.00 sq m.</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Total area :</div>
          <div class="dDesc">3 rai (0.48 hectare, 1.185 acre)</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Number of buildings :</div>
          <div class="dDesc">1 building</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Number of rooms :</div>
          <div class="dDesc">78 units</div>
        </div>
        <div class="dContent">
          <div class="dTitle">All parking :</div>
          <div class="dDesc" id="sectionInstallmentCal">About 70%</div>
        </div>
        <div class="dContent" >
          <div class="dTitle">Common maintenance fee :</div>
          <div class="dDesc">45.00 baht/square meter</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Installment Calculator :</div>

          <div class="dDesc">
            <div class="sectionInstallmentCal">
              <div class="calTitle text-center">
                <h4>Installment Calculator</h4>
              </div>
              <div class="selector text-center">
                <h5>Bank Loans : {{ b.name }}</h5>
                <select
                  class="inputSelector"
                  name=""
                  id=""
                  v-model="bank_active"
                >
                  <option :value="bank" v-for="bank in banks" :key="bank">
                    <img :src="b.image_url" alt="" height="50">{{ bank }}
                  </option>
                </select>
              </div>
              <p class="text-center">Loan amount : 1,700,000 Baht</p>
              <p class="text-center">Loan term : 30 Years</p>
              <div class="imgBank">
                <img class="text-center" :src="b.image_url" alt="" width="300" />
              </div>
              <div class="calContent">
              <div class="row">
                <div class="col-6">
                  <p>Loan amount :</p>
                </div>
                <div class="col-6 text-end">
                  <p>1,700,000 Bath</p>
                </div>
                <hr>
                <div class="col-6">
                  <p>Average interest for the first 3 years :</p>
                  <p>(2.700 - 3.350%)</p>
                  <p>monthly installment</p>
                </div>
                <div class="col-6 text-end">
                  <p>-</p>
                  <p>8,495 - 9,403 baht</p>
                </div>
                <hr>
                <div class="col-6">
                  <p>Real interest over the term of the contract :</p>
                  <p>(4.880 - 5.160%)</p>
                  <p>monthly installment</p>
                </div>
                <div class="col-6 text-end">
                  <p>-</p>
                  <p>11,541 - 11,932 baht</p>
                </div>
              </div>
              <hr>
              <p class="text-muted text-small">
                * Calculation results are examples only. Annuities are subject
                to change according to the borrower's qualifications and bank
                conditions.
              </p>
              <p class="text-muted text-small">
                * Interest rate information update as of 8 Feb. 65
              </p>
              </div>
            </div>
          </div>
        </div>
        <div class="dContent">
          <div class="dTitle">Zone :</div>
          <div class="dDesc">Rayong</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Condominium location :</div>
          <div class="dDesc">
            Moo2 chakpong , Kleng 298, Chakphong, Klaeng, Rayong, Thailand
          </div>
        </div>
        <div class="dContent">
          <div class="dTitle">Public transport :</div>
          <div class="dDesc">Please inquire with the project.</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Nearby landmarks :</div>
          <div class="dDesc">
            Health center, Soonthornphu Monument, Laem Mae Phim Klaeng-Rayong
            District, Soonthornphupittaya School
          </div>
        </div>
        <div class="dContent">
          <div class="dTitle">Year of completion :</div>
          <div class="dDesc">2016</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Telephone Number :</div>
          <div class="dDesc">Tel. 064-556-3644, 038-638-155</div>
        </div>
        <div class="dContent">
          <div class="dTitle">Update on date :</div>
          <div class="dDesc">06/03/2022</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.detailContent a {
  text-decoration: none;
  color: rgb(25, 128, 128);
  font-weight: 600;
}
.detailContent {
  width: 100%;
  padding-bottom: 5em;
}
.dContent {
  padding: 0.5rem 0rem;
  font-size: 1.2rem;
  color: #161616;
}
.dTitle {
  font-weight: 600;
}
.calTitle {
  width: 100%;
  padding-top: 1rem;
  padding-bottom: 0.3rem;
  background: linear-gradient(to bottom right, #fecb17 0%, #cb0201 100%);
  margin-bottom: 1rem;
  h4 {
    color: #fff;
    text-transform: uppercase;
  }
}
.imgBank{
  width: 200px;
  margin: 0 auto;
}
.sectionInstallmentCal {
  border-radius: 5px;
  border: 1px solid #adadad;
}
.inputSelector {
  width: 300px;
  padding: 0.3rem 0.2rem;
  margin: 0.3rem;
  border-radius: 5px;
}
.calContent{
  padding: 2rem;
}
.text-small{
    font-size: 0.95rem;
    color: #493b00 !important;
}
</style>

<script>
export default {
  name: "Fact",
  data() {
    return {
      sectionSubTitle: "get to know us",
      sectionTitle: "Description",
      sectionContent:
        "If you are looking for accommodation in Rayong Easily accessible in excellent locations, Art on the Beach 49 is the answer to where you can easily get to anywhere in this vibrant city.",
      sectionContent2:
        "Because the accommodation is conveniently located. Guests can also visit various popular attractions. Of the city easily. The hotel offers free Wi-Fi in all rooms, 24-hour security, kitchen, Wi-Fi in public areas, laundry service. Maximum guest comfort The accommodation has one beautifully decorated room, some also have a flat screen TV, free coffee, linen, mirror, sofa. The accommodation provides excellent facilities. These include hiking, private beach, fitness room, outdoor pool. Guests can relax after a long drive. Art on the Beach 49 is a great base from which to explore this vibrant city.",
      buttonText: "Installment Calculator",
      // buttonUrl: "/about/#sectionInstallmentCal",
      image: "about-img-6.jpg",
      imageTitle: "We’re committed to trusted Agency",
      imageBtn: "Get Started",
      imageBtnUrl: "/project",
      banks: ["SCB", "BBL", "KBANK", "KTB", "BAY", "UOB", "GSB", "GHB"],
      bank_active: "SCB",
      bank_details: {
        SCB: {
          name: "The Siam Commercial Bank",
          image_url:
            "https://upload.wikimedia.org/wikipedia/en/thumb/4/47/Siam_Commercial_Bank_%28logo%29.svg/1920px-Siam_Commercial_Bank_%28logo%29.svg.png",
        },
        BBL: {
          name: "Bangkok Bank",
          image_url:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/Logo_Bangkok_Bank_Public_Company_Limited.svg/1280px-Logo_Bangkok_Bank_Public_Company_Limited.svg.png",
        },
        KBANK: {
          name: "Kasikorn Bank",
          image_url:
            "https://www.kasikornbank.com/SiteCollectionDocuments/assets/img/logo/kasikornbank.png",
        },
        KTB: {
          name: "Krungthai Bank",
          image_url:
            "https://eprocurement.krungthai.com/procureweb/dist/assets/images/share/ktb3d.png",
        },
        BAY: {
          name: "Bank of Ayudhya",
          image_url:
            "https://upload.wikimedia.org/wikipedia/th/thumb/5/5d/ธนาคารกรุงศรีอยุธยา.png/220px-ธนาคารกรุงศรีอยุธยา.png",
        },
        UOB: {
          name: "United Overseas Bank (UOB)",
          image_url:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/UOB_Logo.svg/2560px-UOB_Logo.svg.png",
        },
        GSB: {
          name: "Government Savings Bank",
          image_url:
            "https://eva.gsb.or.th/gis/assets/images/login_logo_gsb.png",
        },
        GHB: {
          name: "Government Housing Bank",
          image_url:
            "https://www.ghbank.co.th/assets/img/logo-ghb.png",
        },
      },
    };
  },
  computed: {
    b() {
      return this.bank_details[this.bank_active];
    },
  },
};
</script>

<style lang="scss" scoped></style>
