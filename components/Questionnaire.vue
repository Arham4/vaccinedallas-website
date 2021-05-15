<template>
  <div class="p-3">
    <!-- Start Location Selector Area -->
    <b-modal
      v-if="locationSelector === true"
      id="locationSelector"
      size="sm"
      scrollable
      title="Select a location"
      hide-footer
      body-class="p-2"
    >
      <LocationSelector />
    </b-modal>
    <!-- End Location Selector Area -->
    <p>
      All fields are required.
    </p>
    <b-form v-if="show" @submit="onSubmit" @reset="onReset">
      <div v-for="(question, index) in questions">
        <b-form-group :label="question">
          <b-form-radio v-model="chosen[index]" value="Yes" :name="question" required>
            Yes
          </b-form-radio>
          <b-form-radio v-model="chosen[index]" value="No" :name="question" required>
            No
          </b-form-radio>
        </b-form-group>
      </div>
      <b-button v-b-modal.locationSelector type="submit" variant="primary">
        Submit
      </b-button>
      <b-button type="reset" variant="danger">
        Reset
      </b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  components: {
    LocationSelector: () => import('@/components/LocationSelector')
  },
  data () {
    return {
      questions: {
        1: 'In the past 14 days, have you tested positive for COVID-19?',
        2: 'In the past 14 days, have you been in close contact with anyone who tested positive for COVID-19?',
        3: 'Are you currently experiencing fever, coughing, shortness of breath, the new loss of taste or smell, or any other COVID-19 symptoms?',
        4: 'In the past 14 days, have you had a non-COVID-19 vaccination?',
        5: 'In the past 90 days, have you received monoclonal antibodies or convalescent plasma for COVID-19 treatment?',
        6: 'Did you have a severe allergic reaction (e.g., anaphylaxis) to component of the COVID-19 vaccine or after a previous dose?',
        7: 'Did you have a known (diagnosed) allergy to a component of the vaccine or an immediate allergic reaction of any severity to a previous dose?'
      },
      chosen: {},
      show: true,
      locationSelector: false
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      for (const key in this.chosen) {
        const chosen = this.chosen[key]
        if (chosen === 'Yes') {
          alert('You are ineligible to receive the vaccine from us. Please contact your primary care physician.')
          return
        }
      }
      // location.href = 'https://www.solvhealth.com/book-group/VLly3W'
      this.locationSelector = true
    },
    onReset (event) {
      event.preventDefault()
      // Reset our form values
      this.chosen = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>
