<template>
  <v-stepper v-model="e6" vertical>
    <v-stepper-step :complete="e6 > 1" step="1">
      Select an app
      <small>Summarize if needed</small>
    </v-stepper-step>

    <v-stepper-content step="1">
      <template>
      <v-card>
        <v-container fluid>
          <v-row align="center">
            <v-col cols="2" md="1.5">
              <v-select :items="['นาย','นาง.','นางสาว']" label="คำนำหน้า(TH)" dense solo></v-select>
            </v-col>
            <v-col cols="5" md="3">
              <v-text-field label="ชื่อ / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
            <v-col cols="5" md="3">
              <v-text-field label="นามสกุล / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อเล่น / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="2" md="1.5">
              <v-select :items="['Mr.','Mrs.','Miss']" label="คำนำหน้า(EN)" dense solo></v-select>
            </v-col>
            <v-col cols="5" md="3">
              <v-text-field label="Name / (EN)" hint="ระบุเป็นภาษาอังกฤษ" dense outlined></v-text-field>
            </v-col>
            <v-col cols="5" md="3">
              <v-text-field label="Surname / (EN)" hint="ระบุเป็นภาษาอังกฤษ" dense outlined></v-text-field>
            </v-col>
            <v-col cols="2" md="2">
              <v-text-field label="Nickname / (EN)" hint="ระบุเป็นภาษาอังกฤษ" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-subheader>
              วันเกิด
              <br />Date of brith
            </v-subheader>
            <v-col cols="0" md="2">
              <v-text-field label="DD/MM/YYYY" hint="DD/MM/YYYY" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              เพศ
              <br />Sex
            </v-subheader>
            <v-col cols="2" md="1">
              <v-select :items="['Male','Female']" label="Male/Female" dense solo></v-select>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="อายุ/Age" hint="Age" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สัญชาติ
              <br />Nationality
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สัญชาติ/Nationality" hint="Nationality" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-subheader>
              เชื้อชาติ
              <br />Race
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="เชื้อชาติ/Race" hint="Race" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ศาสนา
              <br />Religion
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ศาสนา/Religion" hint="Religion" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ส่วนสูง
              <br />Height
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="ระบุ.." hint="Height" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              น้ำหนัก
              <br />Weight
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="ระบุ.." hint="Weight" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              กรุ๊ปเลือด
              <br />Blood Group
            </v-subheader>
            <v-col cols="2" md="1">
              <v-select :items="['A','B','O','AB']" label dense solo></v-select>
            </v-col>
          </v-row>
          <v-chip class="ma-2">ที่อยู่ปัจจุบัน/ Pressent</v-chip>
          <v-row>
            <v-subheader>
              บ้านเลขที่
              <br />House number
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="บ้านเลขที่" hint="House number" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              หมู่บ้าน/อาคาร
              <br />Village/building
            </v-subheader>
            <v-col cols="3" md="3">
              <v-text-field label="หมู่บ้าน/อาคาร" hint="Village/building" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ซอย
              <br />Alley
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ซอย" hint="Alley" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ถนน
              <br />Street
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ถนน" hint="Street" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              แขวง/ตำบล
              <br />District
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="แขวง/ตำบล" hint="District" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              เขต/อำเภอ
              <br />county
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="เขต/อำเภอ" hint="county" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              จังหวัด
              <br />county
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="จังหวัด" hint="county" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              รหัสไปรษณีย์
              <br />Postal code
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="เขต/อำเภอ" hint="Postal code" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="3" md="3">
              <v-radio-group v-model="type" row>
                <v-radio label="บ้านตนเอง/Own house " dense outlined></v-radio>
                <v-radio label="ห้องเช่า/Rented room" dense outlined></v-radio>
              </v-radio-group>
            </v-col>
          </v-row>
          <v-row>
            <v-subheader>
              Telephone
              <br />โทรศัพท์บ้าน
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="02 .." dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              Mobile
              <br />มือถือ
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="+(66).." dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              Email
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="example@gmail.com" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              Facebook
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label dense outlined></v-text-field>
            </v-col>
          </v-row>
         
          <v-chip class="ma-2">ที่อยู่ตามทะเบียนบ้าน/ Permanent address</v-chip>
          <v-row>
            <v-subheader>
              บ้านเลขที่
              <br />House number
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="บ้านเลขที่" hint="House number" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              หมู่บ้าน/อาคาร
              <br />Village/building
            </v-subheader>
            <v-col cols="3" md="3">
              <v-text-field label="หมู่บ้าน/อาคาร" hint="Village/building" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ซอย
              <br />Alley
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ซอย" hint="Alley" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ถนน
              <br />Street
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ถนน" hint="Street" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              แขวง/ตำบล
              <br />District
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="แขวง/ตำบล" hint="District" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              เขต/อำเภอ
              <br />county
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="เขต/อำเภอ" hint="county" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              จังหวัด
              <br />county
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="จังหวัด" hint="county" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              รหัสไปรษณีย์
              <br />Postal code
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="เขต/อำเภอ" hint="Postal code" dense outlined></v-text-field>
            </v-col>
          </v-row>

          <v-row>
            <v-chip class="ma-2">การอุปสมบท/ Ordination</v-chip>
        <v-radio-group v-model="type" row ><v-radio  label="ไม่เคย/ No" dense outlined
          ></v-radio> <v-radio  label="บวชเรียนแล้ว-ชื่อวัดและที่ตั้ง/ (Yes / where)" dense outlined
      ></v-radio></v-radio-group>

     <v-col cols="3" md="3">
      <v-text-field label="ระบุรายละเอียด" hint="Details" dense outlined></v-text-field> </v-col>
          </v-row>
          <v-row>
              <v-chip class="ma-2">สถานภาพการสมรส/ Marital status</v-chip>
        <v-radio-group v-model="type" row ><v-radio  label="โสด/ Single" dense outlined
          ></v-radio> <v-radio  label="หย้า/ Divorced" dense outlined
      ></v-radio><v-radio  label="หม้าย/ Widowed" dense outlined
      ></v-radio><v-radio  label="สมรสจดทะเบียน/ Civil marriage" dense outlined
      ></v-radio><v-radio  label="สมรสไม่จดทะเบียน/ Common-law marriage" dense outlined
      ></v-radio>
      </v-radio-group>
      </v-row>
      <v-chip class="ma-2">ข้อมูลของคู่สมรสและบุตร / Family information</v-chip>
      <v-row>
          <v-col cols="2" md="1.5">
              <v-select :items="['นาย','นาง']" label="คำนำหน้า" dense solo></v-select>
            </v-col>
          <v-col cols="7" md="3">
              <v-text-field label="ชื่อ / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
            <v-col cols="5" md="3">
              <v-text-field label="นามสกุล / (TH)" hint="ระบุเป็นภาษาไทย" dense outlined></v-text-field>
            </v-col>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="Age" dense outlined></v-text-field>
            </v-col>
            <v-col cols="2" md="2">
              <v-text-field label="อำชีพ/ตำแหน่ง" hint="Occupation / Position" dense outlined></v-text-field>
            </v-col>
            </v-row>
            <v-row>
                 <v-subheader>
              สถำนที่ทำงาน
              <br />Office address
            </v-subheader>
            <v-col cols="2" md="3">
              <v-text-field label="สถานที่ทำงาน" hint="" dense outlined></v-text-field>
            </v-col>
             <v-subheader>
              โทรศัพท์
              <br />Telephone
            </v-subheader>
            <v-col cols="2" md="3">
              <v-text-field label="+66 .." hint="" dense outlined></v-text-field>
            </v-col>
            </v-row>
            <v-row>
<v-chip class="ma-2">จำนวนบุตร / Number of children</v-chip>
<v-col cols="2" md="2">
              <v-select :items="['1','2','3','4','5']" label="จำนวนบุตร" dense solo></v-select>
            </v-col>
            </v-row>
            <v-chip class="ma-2">ประวัติทางครอบครัว (ประวัติของบิดา / มารดา / พี่น้องทุกคน) / Family background</v-chip><br/>
            <v-chip class="ma-2">ควำมสัมพันธ์/ Relation</v-chip>
            <v-row>
                <v-subheader>
              บิดา
              <br />Father
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
           <v-row>
                <v-subheader>
              มารดา
              <br />Father
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
           <v-row>
                <v-subheader>
              พี่น้องลำดับที่1
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
          <v-subheader>
              พี่น้องลำดับที่2
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
          <v-subheader>
              พี่น้องลำดับที่3
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
          <v-subheader>
              พี่น้องลำดับที่4
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
          <v-row>
          <v-subheader>
              พี่น้องลำดับที่5
              <br />
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ชื่อ/นามสกุล" hint="Name" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              อายุ
              <br />Age
            </v-subheader>
            <v-col cols="1" md="1">
              <v-text-field label="อายุ" hint="ระบุเป็นตัวเลข" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              สถานที่ทำงาน/โทรศัพท์
              <br />Company/Telephone
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="สถานที่ทำงาน/โทรศัพท์" hint="Company/Telephone" dense outlined></v-text-field>
            </v-col>
            <v-subheader>
              ตำแหน่ง/อำชีพ
              <br />Position
            </v-subheader>
            <v-col cols="2" md="2">
              <v-text-field label="ตำแหน่ง/อำชีพ" hint="Position" dense outlined></v-text-field>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </template>
      <v-btn color="primary" @click="e6 = 2">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>

    <v-stepper-step :complete="e6 > 2" step="2">Configure analytics for this app</v-stepper-step>

    <v-stepper-content step="2">
      <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
      <v-btn color="primary" @click="e6 = 3">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>

    <v-stepper-step :complete="e6 > 3" step="3">Employment Record 
         <small>ประวัติการทำงาน </small>
    </v-stepper-step>

    <v-stepper-content step="3">
    <v-chip
      class="ma-2" > อันดับที่ 1/ No.1
    </v-chip>
     <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ชื่อ-ที่อยู่บริษัท<br/>Name-<br/>Address Employer</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ประเภทธุรกิจ<br/>Type of Business </p></v-subheader>
      </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ระยะเวลา<br/>Period</p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="2" md="2"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินเดือนล่าสุด<br/>Salary</p></v-subheader>
      </v-col>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินได้พิเศษ<br/>Special Income </p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าพาหนะ/ Travelling expenses " placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     <v-col cols="2" md="2"> <v-text-field  label="ค่าโทรศัพท์/ Mobile" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าคอมมิชชัน/ Commission" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="อื่นๆ/ Other" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ตำแหน่งงานสุดท้าย<br/>Last Position</p></v-subheader>
     </v-col>
    <v-col cols="4" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
 <v-subheader> <p class="font-weight-black">หน้าที่ความรับผิดชอบ<br/>Type of Work</p></v-subheader>
  </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อ-สกุล ผู้บังคับบัญชา<br/>Name of Chief</p></v-subheader>
       </v-col>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-subheader> <p class="font-weight-black">โทรศัพท์ของผู้บังคับบัญชา/Chief's Phone</p> </v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">สาเหตุที่ลาออก<br/>Reason for Leaving</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-chip
      class="ma-2" > อันดับที่ 2/ No.2
    </v-chip>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ชื่อ-ที่อยู่บริษัท<br/>Name-<br/>Address Employer</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ประเภทธุรกิจ<br/>Type of Business </p></v-subheader>
      </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ระยะเวลา<br/>Period</p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="2" md="2"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินเดือนล่าสุด<br/>Salary</p></v-subheader>
      </v-col>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินได้พิเศษ<br/>Special Income </p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าพาหนะ/ Travelling expenses " placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     <v-col cols="2" md="2"> <v-text-field  label="ค่าโทรศัพท์/ Mobile" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าคอมมิชชัน/ Commission" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="อื่นๆ/ Other" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ตำแหน่งงานสุดท้าย<br/>Last Position</p></v-subheader>
     </v-col>
    <v-col cols="4" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
 <v-subheader> <p class="font-weight-black">หน้าที่ความรับผิดชอบ<br/>Type of Work</p></v-subheader>
  </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อ-สกุล ผู้บังคับบัญชา<br/>Name of Chief</p></v-subheader>
       </v-col>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-subheader> <p class="font-weight-black">โทรศัพท์ของผู้บังคับบัญชา/Chief's Phone</p> </v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">สาเหตุที่ลาออก<br/>Reason for Leaving</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-chip
      class="ma-2" > อันดับที่ 3/ No.3
    </v-chip>
    <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ชื่อ-ที่อยู่บริษัท<br/>Name-<br/>Address Employer</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ประเภทธุรกิจ<br/>Type of Business </p></v-subheader>
      </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ระยะเวลา<br/>Period</p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="2" md="2"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินเดือนล่าสุด<br/>Salary</p></v-subheader>
      </v-col>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินได้พิเศษ<br/>Special Income </p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าพาหนะ/ Travelling expenses " placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     <v-col cols="2" md="2"> <v-text-field  label="ค่าโทรศัพท์/ Mobile" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าคอมมิชชัน/ Commission" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="อื่นๆ/ Other" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ตำแหน่งงานสุดท้าย<br/>Last Position</p></v-subheader>
     </v-col>
    <v-col cols="4" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
 <v-subheader> <p class="font-weight-black">หน้าที่ความรับผิดชอบ<br/>Type of Work</p></v-subheader>
  </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อ-สกุล ผู้บังคับบัญชา<br/>Name of Chief</p></v-subheader>
       </v-col>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-subheader> <p class="font-weight-black">โทรศัพท์ของผู้บังคับบัญชา/Chief's Phone</p> </v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">สาเหตุที่ลาออก<br/>Reason for Leaving</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-chip
      class="ma-2" > อันดับที่ 4/ No.4
    </v-chip>
  <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ชื่อ-ที่อยู่บริษัท<br/>Name-<br/> Address Employer</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ประเภทธุรกิจ<br/>Type of Business </p></v-subheader>
      </v-col>
    <v-col cols="12" md="6">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ระยะเวลา<br/>Period</p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="2" md="2"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินเดือนล่าสุด<br/>Salary</p></v-subheader>
      </v-col>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">เงินได้พิเศษ<br/>Special Income </p></v-subheader>
      </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าพาหนะ/ Travelling expenses " placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     <v-col cols="2" md="2"> <v-text-field  label="ค่าโทรศัพท์/ Mobile" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="ค่าคอมมิชชัน/ Commission" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="2" md="2"> <v-text-field  label="อื่นๆ/ Other" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ตำแหน่งงานสุดท้าย<br/>Last Position</p></v-subheader>
     </v-col>
    <v-col cols="4" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
 <v-subheader> <p class="font-weight-black">หน้าที่ความรับผิดชอบ<br/>Type of Work</p></v-subheader>
  </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
        <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อ-สกุล ผู้บังคับบัญชา<br/>Name of Chief</p></v-subheader>
       </v-col>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-subheader> <p class="font-weight-black">โทรศัพท์ของผู้บังคับบัญชา/Chief's Phone</p> </v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">สาเหตุที่ลาออก<br/>Reason for Leaving</p></v-subheader>
     </v-col>
    <v-col cols="12" md="6"> <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>
       </v-row>
       <v-chip
      class="ma-2" > ประวัติการฝึกอบรม-สัมมนา / Training Course - Seminar
    </v-chip>
    <v-row>
     <v-col cols="1">
     <v-chip
      class="ma-2" > ลำดับที่ 1
    </v-chip>
    </v-col> 
    </v-row>
     <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อสถาบัน/Institute</p></v-subheader>
      </v-col>
    <v-col cols="4" md="4">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col> <v-subheader> <p class="font-weight-black">หัวข้อการฝึกอบรม/Course</p></v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    </v-row>
      <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ระยะเวลา/ Period</p></v-subheader>
      </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="3" md="3"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    </v-row>
     <v-chip
      class="ma-2" > ลำดับที่ 2
    </v-chip>
      <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อสถาบัน/Institute</p></v-subheader>
      </v-col>
    <v-col cols="4" md="4">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  <v-subheader> <p class="font-weight-black">หัวข้อการฝึกอบรม/Course</p></v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    </v-row>
      <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ระยะเวลา/ Period</p></v-subheader>
      </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="3" md="3"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    </v-row>
     <v-chip
      class="ma-2" > ลำดับที่ 3
    </v-chip>
     <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ชื่อสถาบัน/Institute</p></v-subheader>
      </v-col>
    <v-col cols="4" md="4">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  <v-subheader> <p class="font-weight-black">หัวข้อการฝึกอบรม/Course</p></v-subheader>
    <v-col cols="2" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    </v-row>
      <v-row>
    <v-col cols="2">
      <v-subheader> <p class="font-weight-black">ระยะเวลา/ Period</p></v-subheader>
      </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="เริ่ม/Since" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
   <v-col cols="3" md="3"> <v-text-field  label="ถึง/Until" placeholder="Details" dense outlined
    ></v-text-field>
    </v-col>
    <v-col cols="3" md="3"> <v-text-field  label="รวม/Total" placeholder="Details"  dense outlined
    ></v-text-field>
    </v-col>
    </v-row>
    <v-chip
      class="ma-2" > บุคคลที่สามารถติดต่อได้ในกรณีฉุกเฉิน / Person to Contact in Case of Emergency
    </v-chip>
     <v-row>
    <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ชื่อ-สกุล<br/>Name-Surname</p></v-subheader>
      </v-col>
    <v-col cols="4" md="4">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  
    <v-subheader> <p class="font-weight-black">ความสัมพันธ์/Relation</p></v-subheader>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
    <v-col cols="2">
    <v-subheader> <p class="font-weight-black">ที่อยู่/Address</p></v-subheader>
     </v-col>
    <v-col cols="4" md="4">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  
     <v-subheader> <p class="font-weight-black">โทรศัพท์/Telephone</p></v-subheader>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  
     </v-row>
      <v-row>
     <v-col cols="2">
     <v-subheader> <p class="font-weight-black">ที่ทำงำน/Office</p></v-subheader>
      </v-col>
    <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  
    <v-subheader> <p class="font-weight-black">ตำแหน่ง<br/>Position</p></v-subheader>
    <v-col cols="2" md="2">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-subheader> <p class="font-weight-black">โทรศัพท์<br/>Telephone</p></v-subheader>
    <v-col cols="2" md="2">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>  
      </v-row>
       <v-chip
      class="ma-2" > ข้อมูลเพิ่มเติม / Miscellaneous
    </v-chip>
     <v-row>
    <v-col cols="5">
     <v-subheader> <p class="font-weight-black">คุณเคยต้องโทษทางอาญาหรือไม่<br />Do you have any criminal or civil record? </p> </v-subheader>
     </v-col>
       <v-radio-group v-model="type" row > 
      <v-radio label="ไม่เคย/ No " dense outlined> 
      </v-radio> 
      <v-radio  label="เคย/ Yes" dense outlined>
      </v-radio></v-radio-group>
     <v-subheader>ระบุ/Explain </v-subheader>
     <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
     <v-col cols="5">
     <v-subheader> <p class="font-weight-black">คุณเคยสมัครงานหรือทำงานกับบริษัทมาก่อนหรือไม่<br />Have you ever applied to this company?</p></v-subheader>
     </v-col>
        <v-radio-group v-model="type" row >
        <v-radio  label="ไม่เคย/ No " dense outlined >
        </v-radio> 
        <v-radio  label="เคย/ Yes" dense outlined
      ></v-radio></v-radio-group>
     <v-subheader>ระบุ/Explain </v-subheader>
     <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="5">
     <v-subheader> <p class="font-weight-black">คุณเคยป่วยหนักหรือเป็นโรคติดต่อร้ายแรงหรือไม่<br />Have you ever been seriously ill or contracted with contagious disease?</p></v-subheader>
     </v-col>
        <v-radio-group v-model="type" row >
       <v-radio  label="ไม่เคย/ No " dense outlined >
     </v-radio>
     <v-radio  label="เคย/ Yes" dense outlined
      ></v-radio></v-radio-group>
     <v-subheader>ระบุ/Explain </v-subheader>
     <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
     <v-col cols="5">
     <v-subheader> <p class="font-weight-black">บริษัทสามารถพูดคุยกับนายจ้างเดิมของคุณได้หรือไม่<br />Can we contact your past employer?</p> </v-subheader>
      </v-col>
        <v-radio-group v-model="type" row >
         <v-radio  label="ได้/ Yes" dense outlined>
         </v-radio>
         <v-radio  label="ไม่ได้/ No" dense outlined
      ></v-radio></v-radio-group>
     <v-subheader>เพราะ/ Because </v-subheader>
     <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
      <v-row>
    <v-col cols="5">
     <v-subheader> <p class="font-weight-black">บุคคลในบริษัทที่คุณรู้จัก<br />Relatives or friends working in this company</p></v-subheader>
      </v-col>
        <v-radio-group v-model="type" row >
        <v-radio  label="มี/ Yes" dense outlined>
        </v-radio> 
        <v-radio  label="ไม่มี/ No" dense outlined
      ></v-radio></v-radio-group>
     <v-subheader>ชื่อ/ Name</v-subheader>
     <v-col cols="3" md="3">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     </v-row>
     <v-row>
      <v-col cols="5">
        <v-subheader> <p class="font-weight-black">ข้อความเพิ่มเติมอื่น ๆ ที่ประสงค์จะแจ้งให้ทราบ<br />Additional information</p></v-subheader>
      </v-col>
      <v-col cols="5" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    </v-row>
     <v-row>
     <v-col cols="5">
     <v-subheader> <p class="font-weight-black">เงินเดือนที่ต้องการ/Salary Expectation</p> </v-subheader>
     </v-col>
      <v-col cols="5" md="5">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    </v-row>

      <v-btn color="primary" @click="e6 = 4">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>

    <v-stepper-step step="4">คำถามจากบริษัท VSTECS <small>กรุณาตอบคำถามตามความคิดเห็นอย่างตรงไปตรงมาที่สุด</small></v-stepper-step>
    <v-stepper-content step="4">
     <v-chip
      class="ma-2" > กรุณาตอบคำถามตามความคิดเห็นอย่างตรงไปตรงมาที่สุด
    </v-chip>
    <v-subheader><p class="font-weight-black">1). อะไรที่ทำให้คุณอยากเปลี่ยนงานใหม่</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">2). อะไรที่ทำให้คุณสนใจมาสมัครงานที่นี่</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">3). คุณคิดว่าตัวคุณเหมาะสมกับตำแหน่งที่คุณสมัครอย่างไรบ้าง</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">4). ในการทำงานที่ผ่านมาคุณได้ตั้งเป้าหมายในการทำงานหรือไม่ และประสบความสำเร็จตามเป้าหมายมากน้อยเพียงใด</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">5). อธิบายความหมายของ “คิดบวกเชิงสร้างสรรค์” ในความคิดของคุณ</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">6). อธิบายความหมายของ “จริงใจในสิ่งที่ทำ” ในความคิดของคุณ</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">7). อธิบายความหมายของ “ทำงานอย่างมืออาชีพ” ในความคิดของคุณ</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">8). อธิบายความหมายของ “เป็นเจ้าของร่วมกัน” ในความคิดของคุณ</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">9). อธิบายความหมายของ “รวมพลังเป็นหนึ่งเดียว” ในความคิดของคุณ</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">10).ผลงานใดที่ทำให้คุณภาคภูมิใจมากที่สุด</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">11). หากคุณเลือกได้คุณอยากมีหัวหน้าแบบใด</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">12). หากคุณเลือกได้คุณอยากได้ลูกน้องแบบใด</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">13). เมื่อคุณประสบปัญหาในการทำงาน (หรือชีวิต) มากที่สุด จนรู้สึกท้อถอย คุณมีวิธีการแก้ไขสถานการณ์นั้นอย่างไร</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
    <v-subheader><p class="font-weight-black">14). คุณคิดว่าอยากจะพัฒนาตนเองในเรื่องใดมากที่สุด เพราะอะไร</p></v-subheader>
    <v-col cols="2" md="10">
      <v-text-field label="Details" hint="Details" dense outlined></v-text-field>
    </v-col>
     <v-chip
      class="ma-2" > English Writing
    </v-chip>
    <v-subheader> <p class="font-weight-black">Please choose 1 topic for paragraph writing about 100 words or 10 sentences</p></v-subheader>
    <v-subheader> <p class="font-weight-black">1). My life in next 5 years</p></v-subheader>
    <v-subheader> <p class="font-weight-black">2). If I could turn back time</p></v-subheader>
    <v-subheader> <p class="font-weight-black">3). My dream boss</p></v-subheader>
    <p class="font-weight-medium"></p>
     <v-col cols="2" md="10">
          <v-textarea outlined  name="input-8-5" label="Details" hint="Details"
        ></v-textarea>
      </v-col>


      <v-btn color="primary" @click="e6 = 1">Continue</v-btn>
      <v-btn text>Cancel</v-btn>
    </v-stepper-content>
  </v-stepper>
</template>
<script>
  export default {
    data () {
      return {
        e6: 1,
      }
    },
  }
</script>
