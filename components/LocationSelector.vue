<template>
  <div>
    <b-form-select v-model="selected" :options="options" />
    <b-button variant="primary" :href="selected" style="margin-top: 10px">
      Submit
    </b-button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      selected: null,
      options: [
        { value: null, text: 'Please select a location' },
        { value: 'https://www.solvhealth.com/book-online/0r3GjA', text: 'Frisco' },
        { value: 'https://www.solvhealth.com/book-online/0xwYGg', text: 'Garland' }
      ]
    }
  }
}
</script>
