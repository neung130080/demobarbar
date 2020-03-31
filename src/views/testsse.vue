<template>
  <v-stepper v-model="e6" vertical>
    <v-stepper-step :complete="e6 > 1" step="1">
      Profile
      <small>ประวัติส่วนบุคคล</small>
    </v-stepper-step>
    
    <v-col cols="5" md="3">
      <v-text-field
        label="Prepend inner"
        prepend-inner-icon="mdi-human-male"
        hint="Job description"
        dense
        outlined
      >></v-text-field>
      <v-text-field label="Job Details" hint="Job description" dense outlined>></v-text-field>
    </v-col>
    <v-col cols="5" md="3">
      <v-text-field label="Job Details" hint="Job description" dense outlined></v-text-field>
    </v-col>

    <v-btn color="primary" @click="e6 = 2">Continue</v-btn>
    <v-btn text>Cancel</v-btn>

    <v-stepper-step :complete="e6 > 2" step="2">Educational background<small>ประวัติการศึกษา</small></v-stepper-step>

    <v-stepper-content step="2">
     
      <v-btn color="primary" @click="e6 = 3">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>

    <v-stepper-step :complete="e6 > 3" step="3">Select an ad format and name ad unit</v-stepper-step>

    <v-stepper-content step="3">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 4">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>

    <v-stepper-step step="4">View setup instructions</v-stepper-step>
    <v-stepper-content step="4">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 1">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>
  </v-stepper>
</template>
<script>
export default {
  data() {
    return {
      e6: 1
    };
  }
};
</script>