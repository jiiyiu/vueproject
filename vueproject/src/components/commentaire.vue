<template>
  <div>
      <v-layout
          align-center
          justify-center
        >
      <v-col
     cols="9"
        >
         <br/><h2 class="text-center font-weight-thin">Lorem ipsum dolor sit amet</h2><br/>
    <b-form-textarea
      id="textarea"
      v-model="text"
      placeholder="Enter something..."
      rows="3"
      max-rows="6"
    ></b-form-textarea>
    <p class="font-italic mb-9 dark " >Message:</p>

    <pre class="mt-3 mb-0">{{ text }}</pre>
      </v-col>
      </v-layout>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        text: ''
      }
    }
  }
</script>