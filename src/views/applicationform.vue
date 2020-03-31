<template>
  <v-timeline :dense="$vuetify.breakpoint.smAndDown">
    <v-timeline-item color="purple lighten-2" fill-dot right>
      <v-card>
        <v-card-title class="purple lighten-2">
          <v-icon dark size="42" class="mr-4">mdi-magnify</v-icon>
          <h2 class="display-1 white--text font-weight-light">Personal information</h2>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col cols="4" md="3">
              <v-select :items="['นาย','นาง','นางสาว']" label="คำนำหน้า" dense solo></v-select>
            </v-col>
            <v-col cols="12" md="7">
              <v-text-field label="ชื่อ / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
              <v-text-field label="นามสกุล / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="3">
              <v-select :items="['Mr.','Mrs.','Miss.']" label="คำนำหน้า (EN)" dense solo></v-select>
            </v-col>
            <v-col cols="10" md="7">
              <v-text-field label="Name / (EN)" hint="ระบุเป็นภาษาอังกฤษ" dense outlined></v-text-field>
              <v-text-field label="Surname / (EN)" hint="ระบุเป็นภาษาอังกฤษ" dense outlined></v-text-field>
            </v-col>
            <v-col cols="10" md="5">
              <v-text-field label="นามสกุล / (TH)" hint="ระบุเป็นภาษาไทย" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="Mr./Mrs./Miss" hint="(EN)ห้าม! ใส่อักษรย่อ" outlined></v-text-field>
            </v-col>
            <v-col cols="10" md="5">
              <v-text-field label="Name / (EN)" hint="ระบุเป็นภาษาอังกฤษ" outlined></v-text-field>
            </v-col>
            <v-col cols="10" md="5">
              <v-text-field label="Lastname / (EN)" hint="ระบุเป็นภาษาอังกฤษ" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>
            <v-col cols="4" md="2">
              <v-text-field label="อายุ / Age" hint="ระบุเป็นตัวเลข" outlined></v-text-field>
            </v-col>

            <v-col class="hidden-sm-and-down text-right" md="2">
              <v-icon size="64">mdi-calendar-text</v-icon>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="amber lighten-1" fill-dot left small>
      <v-card>
        <v-card-title class="amber lighten-1 justify-end">
          <h2 class="display-1 mr-4 white--text font-weight-light">Educational background</h2>
          <v-icon dark size="42">mdi-home-outline</v-icon>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col cols="12" md="5">
              <v-text-field label="Job Details" hint="Job description" outlined></v-text-field>
              <v-text-field label="Job Details" hint="Job description" outlined></v-text-field>
            </v-col>
            <v-col cols="14" md="7">
              <v-text-field label="Job Details" hint="Job description" outlined></v-text-field>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="cyan lighten-1" fill-dot right>
      <v-card>
        <v-card-title class="cyan lighten-1">
          <v-icon class="mr-4" dark size="42">mdi-email-outline</v-icon>
          <h2 class="display-1 white--text font-weight-light">Work history</h2>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col
              v-for="n in 3"
              :key="n"
              cols="12"
              md="4"
            >Lorem ipsum dolor sit amet, no nam oblique veritus no nam oblique.</v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="red lighten-1" fill-dot left small>
      <v-card>
        <v-card-title class="red lighten-1 justify-end">
          <h2 class="display-1 mr-4 white--text font-weight-light">Questions from the company</h2>
          <v-icon dark size="42">mdi-account-multiple-outline</v-icon>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col class="hidden-sm-and-down" md="2">
              <v-icon size="64">mdi-server-network</v-icon>
            </v-col>
            <v-col
              cols="12"
              md="10"
            >Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus.</v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="green lighten-1" fill-dot right>
      <v-card>
        <v-card-title class="green lighten-1">
          <v-icon class="mr-4" dark size="42">mdi-phone-in-talk</v-icon>
          <h2 class="display-1 white--text font-weight-light">สามารถติดต่อเราได้ที่</h2>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col>Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.</v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>