<template>
  <div class="main-container">
    <HeaderElement />

    <OffCanvasMobileMenu />

    <!-- Start Hero Slider Area -->
    <div class="hero-item hero-item-corona" :style="{ backgroundImage: `url('/img/bg/front_main_bg.png')` }">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="hero-content-5 left">
              <h3>Drive-Thru <br> COVID-19 <br> Vaccines</h3>
              <p>We're administering the vaccine by appointment only.</p>
              <b-button v-b-modal.questionnaire class="brook-btn bk-btn-theme btn-sd-size btn-rounded corona-btn space-between" @click="questionnaire = true">
                Schedule appointment
              </b-button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Hero Slider Area -->

    <!-- Start Questionnaire Area -->
    <b-modal
      v-if="questionnaire === true"
      id="questionnaire"
      size="xl"
      scrollable
      title="Before we schedule your vaccine(s)"
      hide-footer
      body-class="p-2"
    >
      <Questionnaire />
    </b-modal>
    <!-- End Questionnaire Area -->

    <!-- Start Eligibility Area -->
    <div class="eligibility-area bg_color--1 pt--110 pt_md--80 pt_sm--60 pb--90 pb_md--55 pb_sm--30">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 col-md-12 col-sm-12 col-12">
            <div class="thumbnail wow move-up animate">
              <img src="/img/eligibility/injection.jpg" alt="doctor injecting vaccine to a patient">
            </div>
          </div>
          <div class="col-lg-6 col-md-12 col-sm-12 col-12">
            <div class="eligibility-content wow move-up animate">
              <!-- Section Title Start -->
              <div class="brook-section-title-corona mb--50">
                <h2>Are you eligible to <br> be administered the <br> <span class="text-black text-underline">COVID-19 vaccine</span>?</h2>
                <p>
                  As of Monday, March 29, 2021, <b>all vaccines are authorized for people age 18 and older. The Pfizer vaccine is authorized for people 16 and older.</b>
                </p>
              </div>
              <!-- Section Title End -->
              <!-- Single Eligibility Start -->
              <div class="single-eligibility mb--30">
                <div class="eligibility-image rotate-center">
                  <img src="/img/eligibility/old.png" alt="People 65+ or people 16+ with a health condition">
                </div>
                <div class="eligibility-content">
                  <h3 class="title">
                    Phase 2
                  </h3>
                  <p>
                    All vaccines are authorized for people age 18 and older. The Pfizer vaccine is authorized for people 16 and older.
                  </p>
                </div>
              </div>
              <!-- Single Eligibility End -->
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Eligibility Area -->
    <!-- Vaccine Location Start -->
    <div class="vaccine-location pb--120 pb_md--80 pb_sm--60">
      <div class="container">
        <div class="row">
          <div class="col-12 position-relative wow move-up animate">
            <div class="corona-map-area">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3340.809769463977!2d-96.80773258480863!3d33.14036188086376!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x864c3c47807b1873%3A0x4a697a477bac6527!2sFrisco%20Medical%20Office%20Building%2C%207589%20Preston%20Rd%2C%20Frisco%2C%20TX%2075034!5e0!3m2!1sen!2sus!4v1616518999502!5m2!1sen!2sus"
                width="1170"
                height="600"
                style="border:0;"
                allowfullscreen=""
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Vaccine Location End -->
    <FooterTwo />
  </div>
</template>

<script>
export default {
  components: {
    Questionnaire: () => import('@/components/Questionnaire'),
    HeaderElement: () => import('@/components/HeaderElement'),
    OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
    FooterTwo: () => import('~/components/Footer')
  },

  data () {
    return {
      questionnaire: false
    }
  },

  mounted () {
    document.body.classList.add('template-color-41', 'template-font-3')
  },

  head () {
    return {
      title: 'VaccineDallas - Drive-thru COVID-19 vaccine'
    }
  }
}
</script>

<style lang="scss" scoped>
.single-symptom {
  background: url('../static/img/design.png');
  background-color: #F9F2FF;
  background-position: right;
  background-repeat: no-repeat;
}
</style>
