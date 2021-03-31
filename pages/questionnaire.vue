<template>
  <div class="main-container">
    <HeaderElement />

    <OffCanvasMobileMenu />

    <Breadcrumb :items="items" title="Booking Questionnaire" />

    <div class="eligibility-area bg_color--1 pt--110 pt_md--80 pt_sm--60 pb--90 pb_md--55 pb_sm--30">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 col-md-12 col-sm-12 col-12">
            <div class="thumbnail wow move-up animate">
              <img src="/img/questionnaire/injection.png" alt="doctor injecting vaccine to a patient">
            </div>
          </div>
          <div class="col-lg-6 col-md-12 col-sm-12 col-12">
            <div class="eligibility-content wow move-up animate">
              <Questionnaire />
            </div>
          </div>
        </div>
      </div>
    </div>

    <FooterTwo />
  </div>
</template>

<script>
export default {
  components: {
    Questionnaire: () => import('@/components/Questionnaire'),
    HeaderElement: () => import('@/components/HeaderElement'),
    OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
    FooterTwo: () => import('@/components/Footer'),
    Breadcrumb: () => import('@/components/Breadcrumb')
  },

  data () {
    return {
      items: [
        {
          text: 'Home',
          to: '/'
        },
        {
          text: 'Book',
          active: true
        }
      ]
    }
  },

  head () {
    return {
      title: 'VaccineDallas - Booking Questionnaire'
    }
  }
}
</script>
