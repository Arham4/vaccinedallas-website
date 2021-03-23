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
              <h3>Protect yourself <br> & your family <br> from COVID-19</h3>
              <p>We're administering the vaccine by appointment only <br> based on local eligibility guidelines.</p>
              <n-link to="#" class="brook-btn bk-btn-theme btn-sd-size btn-rounded corona-btn space-between">
                Schedule appointment
              </n-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Hero Slider Area -->

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
                <p>Texas authorities have developed guidelines to prioritize
                  <span class="text-black text-underline">vulnerable populations</span> in the first phase of the
                  distribution of COVID-19 vaccines. The following are eligible now:</p>
              </div>
              <!-- Section Title End -->

              <!-- Single Eligibility Start -->
              <div class="single-eligibility mb--30">
                <div class="eligibility-image">
                  <img src="/img/eligibility/healthcare.png" alt="healthcare workers">
                </div>
                <div class="eligibility-content">
                  <h3 class="title">
                    Phase 1A
                  </h3>
                  <p>Front-line healthcare workers and residents at long-term care facilities</p>
                </div>
              </div>
              <!-- Single Eligibility End -->
              <!-- Single Eligibility Start -->
              <div class="single-eligibility mb--30">
                <div class="eligibility-image rotate-center">
                  <img src="/img/eligibility/old.png" alt="People 65+ or people 16+ with a health condition">
                </div>
                <div class="eligibility-content">
                  <h3 class="title">
                    Phase 1B
                  </h3>
                  <p>People 65+ or people 16+ with a health condition that increases risk of severe COVID‑19 illness. A
                    list of all health conditions can be found <a href="https://www.cdc.gov/coronavirus/2019-ncov/need-extra-precautions/people-with-medical-conditions.html">here</a>.</p>
                </div>
              </div>
              <!-- Single Eligibility End -->
              <!-- Single Eligibility Start -->
              <div class="single-eligibility mb--30">
                <div class="eligibility-image">
                  <img src="/img/eligibility/middleage.png" alt="People 50 to 64 years of age">
                </div>
                <div class="eligibility-content">
                  <h3 class="title">
                    Phase 1C
                  </h3>
                  <p>
                    People 50 to 64 years of age
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
              <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3340.809769463977!2d-96.80773258480863!3d33.14036188086376!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x864c3c47807b1873%3A0x4a697a477bac6527!2sFrisco%20Medical%20Office%20Building%2C%207589%20Preston%20Rd%2C%20Frisco%2C%20TX%2075034!5e0!3m2!1sen!2sus!4v1616518999502!5m2!1sen!2sus" width="1170" height="600" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
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
    HeaderElement: () => import('@/components/HeaderElement'),
    OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
    FooterTwo: () => import('~/components/Footer')
  },

  mounted () {
    document.body.classList.add('template-color-41', 'template-font-3')
  },

  head () {
    return {
      title: 'VaccineDallas'
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
