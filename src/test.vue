 <template>
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="indigo lighten-2" dark flat>
                <v-toolbar-title>Login form</v-toolbar-title>
                <v-spacer />
                
                
                
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-col cols="12" >
                  <v-text-field label="Username"
                hint="เลขประจำตัว 13 หลัก /ID code 13"
                outlined/>
                   </v-col>
                    <v-col cols="12" >
                  <v-text-field label="Email"
                hint="ระบุอีเมลที่สามารถติดต่อได้"
                outlined/>
                   </v-col>
                    <v-col cols="12" >
                  <v-text-field label="numberphone"
                hint="หมายเลขโทรทัพศ์ที่สามรถติดต่อได้"
                outlined/>
                   </v-col>
                  <v-col cols="12" >
                  <v-text-field label="Password"
                hint="ระบุตัวเลข หรือ ตัวอีกษร 6-8 ตัว"
                outlined/>
                   </v-col>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn color="red lighten-4">Login</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  props: {
    source: String
  }
};
</script>