<template>
  <div class="map">
    <div class="title_area _english_font _big_text _black">
      Location
    </div>
    <div class="_big_text _black">
      <b>Akses</b>
    </div>

    <div class="address_area _large_text _gray">
      Perumahan Taman Wanasari Indah<br>
      Blok B2 No 5 RT 009 RW 008<br>
      <p>Cibitung, Bekasi 17520</p>
    </div>

    <a style="cursor: pointer" @click="copyAddress">
      <img class="addr_btn" src="../assets/images/new/map/aadr_btn.png" />
    </a>

    <div class="bottom center ui toast-container _toast" v-show="showCopyCompleteModal">
      <div class="floating toast-box" style="text-align: left">
        <div role="alert" class="ui toast compact _toast_color" style="opacity: 1;">
          <i class="copy icon" style="visibility: visible;"></i>
          <div class="content">
            <div class="message">Penyalinan selesai.</div>
          </div>
        </div>
      </div>
    </div>



    <iframe
        class="_google_map_iframe"
        :src="googleMapSrc"
        allowFullScreen="" loading="lazy"
        referrerPolicy="no-referrer-when-downgrade">
    </iframe>

    <div class="util_btn_icon_area">
      <a :href="tmapUrl">
        <img class="util_btn_icon" src="../assets/images/new/map/maps.png"/>
      </a>
    </div>

    <div class="map_desc_area _tiny_text _gray">
      <Divider3 :padding-bottom="0" padding-right="44"/>
    </div>


  </div>
</template>

<script>

import Divider3 from "@/components/Divider3.vue";

export default {
  name: "google-map-area",
  components : {
    Divider3
  },
  data() {
    return {
      locationName: "Mama Resti",
      address : "Perumahan Taman Wanasari Indah Blok B2 No 5 RT 009 RW 008",
      showCopyCompleteModal: false,
      tmapUrl: "",
      kakaoTaxiUrl: "",
      navermapUrl: "",
      kakaomapUrl: "",
      googleMapSrc: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.19872842079!2d107.09565467589161!3d-6.2375170937507445!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e698f00112c051f%3A0xbe74c7c74b5cce2a!2sMama%20Resti!5e0!3m2!1sid!2sjp!4v1716809089496!5m2!1sid!2sjp",
    }
  },
  mounted() {
    this.makeUrls()
  },
  methods: {
    makeUrls() {
      const locationName = this.locationName
      this.tmapUrl = "https://www.google.com/maps/place/Mama+Resti,+Jl.+Taman+Wanasari+Indah+No.05+Blok+B2,+Wanasari,+Kec.+Cibitung,+Kabupaten+Bekasi,+Jawa+Barat+17520,+Indonesia/@-6.2375171,107.0982296,16z/data=!4m6!3m5!1s0x2e698f00112c051f:0xbe74c7c74b5cce2a!8m2!3d-6.2375171!4d107.0982296!16s%2Fg%2F11ldwdptrc"
      this.kakaoTaxiUrl = "https://t.kakao.com/launch?type=taxi&amp;dest_lat=37.49878007763176&amp;dest_lng=127.03170076652506&amp;ref=localweb"
      this.navermapUrl = "nmap://search?query=" + locationName
      this.kakaomapUrl = "kakaomap://search?q=" + locationName
    },
    copyAddress() {
      this.$copyText(this.address).then(() => {
        this.showCopyCompleteModal = true
        setTimeout(() => {
          this.showCopyCompleteModal = false
        }, 1000)
      })
    }
  }
};
</script>

<style lang="scss" scoped>

.map {
  margin-top: 18px;
  margin-bottom: 18px;
  text-align: center;
}

.title_area {
  margin-top: 56px;
  line-height: 24px;
  color: #797979;
  margin-bottom: 8px;
}


.address_area {
  margin-top: 16px;
  line-height: 30px;
  p {
    margin-top: 4px;
  }
}

.addr_btn {
  width: 82px;
  height: 44px;
  margin-top: 24px;
  line-height: 28px;
  margin-bottom: 48px;
}

._toast {
  bottom: 300px!important;
}

._toast_color {
  background-color: #4d7846!important;
  opacity: 0.9!important;
  color: white!important;
}

._google_map_iframe {
  margin-left: 10px;
  margin-right: 10px;
  border: 0;
  width: 80%;
  min-height: 310px;
  min-width: 320px;
}

.util_btn_icon_area {
  margin-top: 16px;
}

.util_btn_icon {
  width: 113px;
  height: 46px;
  background: var(--secondary-bg-color);
}

.map_desc_area {
  text-align: left;
  margin-top: 56px;
  margin-left: 43px;
  line-height: 28px;
}

</style>
