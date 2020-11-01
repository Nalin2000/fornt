<template>
  <v-container>
    <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>
    <v-container class="mt-12 mb-3">
      <h2 id="room" class="nav--text font-weight-regular">
        <v-icon size="70" color="nav">mdi-seat-individual-suite </v-icon>
        <b>THE BEST FRONT BEACH ROOMS</b>
      </h2>
      <v-row>
        <v-col cols="12" md="6">
          <v-img src="/13.jpg"></v-img>
        </v-col>
        <v-col md="1"></v-col>
        <v-col cols="12" md="5">
          <h3 class="nav--text font-weight-thin">
            &emsp;&emsp;ห้องพักที่ออกแบบอย่างลงตัว ในความหรูหรา เรียบง่าย
            ไม่เหมือนใคร บรรยากาศเงียบสงบเป็นส่วนตัว
            ผสานสิ่งอำนวยความสะดวกครบครัน
            เหมาะสำหรับทริปพักผ่อนของคู่รักอย่างแท้จริง <br />
            <br />
            <v-icon size="30" color="nav">mdi-circle-slice-8 </v-icon>
            &nbsp;ห้องนอน ขนาดใหญ่ 80 ตรม. <br />
            <v-icon size="30" color="nav">mdi-circle-slice-8 </v-icon>
            &nbsp;เตียงนอนคิงไซส์และผ้าขนหนูนิลินคุณภาพดี<br />
            <v-icon size="30" color="nav">mdi-circle-slice-8 </v-icon>
            &nbsp;ราคาเพียง 890 บาท/คืน <br />
            <v-icon size="30" color="nav">mdi-circle-slice-8 </v-icon>
            &nbsp;จำนวน 10 ห้อง
          </h3>
        </v-col>
      </v-row>
    </v-container>
    <v-divider color="#616161"></v-divider>
    <v-container class="mt-6">
      <h2 id="Facilitate" class="nav--text font-weight-regular">
        <b> Facilitate</b>
      </h2>
      <v-row>
        <v-col cols="12" md="6">
          <v-img src="/14.jpg"></v-img>
        </v-col>
        <v-col md="1"></v-col>
        <v-col cols="12" md="5">
          <h3 class="nav--text font-weight-thin">
            <v-row
              ><v-col cols="12"
                ><v-icon size="30" color="nav">mdi-cctv </v-icon>
                &nbsp;ระบบรักษาความปลอดภัย 24 ชั่วโมง<br
              /></v-col>
              <v-col cols="12"
                ><v-icon size="30" color="nav">mdi-wifi </v-icon>
                &nbsp;ฟรีบริการอินเตอร์เน็ตไร้สาย (Wi-Fi)<br
              /></v-col>
              <v-col cols="12" md="6"
                ><v-icon size="30" color="nav">mdi-card-text </v-icon>
                &nbsp;ระบบคีย์การ์ด<br
              /></v-col>
              <v-col cols="12" md="6"
                ><v-icon size="30" color="nav"
                  >mdi-room-service-outline
                </v-icon>
                &nbsp;อาหารเช้าฟรี<br
              /></v-col>
              <v-col cols="12" md="6"
                ><v-icon size="30" color="nav">mdi-pool </v-icon>
                &nbsp;อ่างจากุซซี่<br /></v-col
            ></v-row>
          </h3>
        </v-col>
      </v-row>
    </v-container>
    <v-container class="mt-12">
      <h2 id="gallary" class="nav--text font-weight-regular text-center">
        <v-icon size="60" color="nav">mdi-camera-iris</v-icon> GALLARY
      </h2>
      <v-divider color="#616161"></v-divider>
      <v-row
        ><v-col v-for="(image, i) in imageS" :key="i" col="6" md="4" sm="6"
          ><v-img :src="image.src"></v-img></v-col
      ></v-row>
    </v-container>
    <v-divider color="#616161"></v-divider>
    <v-row class="mt-6"
      ><v-col cols="12" md="6"
        ><h2 id="contact" class="nav--text font-weight-regular">
          <b> CONTACT</b>
        </h2>
        <h3 class="nav--text font-weight-medium">
          <v-row
            ><v-col cols="12"
              ><v-icon size="30" color="nav">mdi-phone </v-icon> &nbsp;055
              313343<br
            /></v-col>
            <v-col cols="12"
              ><v-icon size="30" color="nav">mdi-email-outline </v-icon> &nbsp;
              lynnhotel@gmail.com<br
            /></v-col>
            <v-col cols="12"
              ><v-icon size="30" color="nav">mdi-facebook </v-icon> &nbsp;LYNN
              Hotel<br
            /></v-col>
            <v-col cols="12"
              ><v-icon size="30" color="nav">mdi-comment-outline </v-icon>
              &nbsp;Line: @lynnHotel (มี @)<br
            /></v-col>
            <v-col cols="12"
              ><v-icon size="30" color="nav">mdi-map-marker-radius </v-icon>
              &nbsp;ต.หนองแก อ.หัวหิน จ.ประจวบคีรีขันท์ 77110<br /></v-col
          ></v-row>
        </h3>
      </v-col>
      <v-col cols="12" md="6"
        ><h2 id="Facilitate" class="nav--text font-weight-regular">
          ห้องว่างวันนี้
        </h2>
        <state /></v-col
    ></v-row>
  </v-container>
</template>

<script>
import state from '@/components/state'
export default {
  state,
  data() {
    return {
      items: [
        {
          src: '/20.jpg',
        },
        {
          src: '/21.jpg',
        },
        {
          src: '/22.jpg',
        },
        {
          src: '/23.jpg',
        },
        {
          src: '/5.jpg',
        },
      ],
      imageS: [
        {
          src: '/12.jpg',
        },
        {
          src: '/13.jpg',
        },
        {
          src: '/7.jpg',
        },
        {
          src: '/8.jpg',
        },
        {
          src: '/9.jpg',
        },
        {
          src: '/10.jpg',
        },
      ],
    }
  },
}
</script>

<style scoped>
h3.dis {
  margin-left: auto;
  margin-right: auto;
}
</style>
