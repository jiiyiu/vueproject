<template>
 <v-form v-model="valid">
    <v-container>
       <v-layout
          align-center
          justify-center
        >
      <v-row >
        <v-col
          cols="15"
          md="5"
        >
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            :counter="10"
            label="First name"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="15"
        >
          <v-text-field
            v-model="lastname"
            :rules="nameRules"
            :counter="10"
            label="Last name"
            required
          ></v-text-field>
        </v-col>

      </v-row>
      </v-layout>
      <p>Vous etes: {{firstname |capitalize}} {{lastname |capitalize}}</p>
    </v-container>
  </v-form>
</template>


<script>
    export default {
        data() {
          
            return {
                select: '',
                firstname: '',
                lastname: ''
            }
        },
        filters: {
            capitalize: function(value) {
                if (!value) return ''
                value = value.toString()
                return value.charAt(0).toUpperCase() + value.slice(1)
            }
        }
    } 
</script>
