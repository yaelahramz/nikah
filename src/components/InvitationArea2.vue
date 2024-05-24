<template>
  <div class="invitation_area">
    <p class="header _big_text _green">
      <strong>"QS Ar Rum 21"</strong><br />
    </p>
    <div class="desc _large_text _gray">
Di antara tanda-tanda (kebesaran)-Nya ialah bahwa Dia menciptakan pasangan-pasangan untukmu dari (jenis) dirimu sendiri agar kamu merasa tenteram kepadanya. Dia menjadikan di antaramu rasa cinta dan kasih sayang. Sesungguhnya pada yang demikian itu benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.<br />
    </div>

    <Divider3 :padding-bottom="0" padding-right="24" padding-left="24"/>

    <div class="names _small_text _gray">
      <p><strong>Resti Kurniawati</strong></p>
      <p><span class="male">Putri Kedua dari Bapak Satam Ibu Jubaedah</span></p>
      <p>(故)박복식∙신미애<span class="male">의 차남</span><strong>성수</strong></p>
      <p>김동균∙송인숙<span class="male">의 장녀</span><strong>규빈</strong></p>
    </div>

    <img class="invi_main_image" src="../assets/images/new/invitation/invi_img.png" />

  </div>
</template>

<script>

import Divider3 from "@/components/Divider3.vue";

export default {
  name: "invitation-area",
  components: {
    Divider3,
  },
  methods: {
  },
};
</script>

<style lang="scss" scoped>
.invitation_area {
  background: var(--secondary-bg-color);
  text-align: center;
  line-height: 0;
  .header {
    padding-top: 56px;
    line-height: 28px;
  }
  .desc {
    line-height: 30px;
    padding-bottom: 36px;
  }
  .line_area {
    padding-bottom: 36px;
  }
  .line {
    width: 382px;
    border: 0.7px solid;
    color: #D7D7D7;
  }
  .names {
    text-align: center;
    line-height: 0;
    letter-spacing: 3px;
    margin-top: 24px;
    padding-right: 68px;
    .male {
      font-size: 12.5px;
      margin-left: 26px;
      margin-right: 43px;
    }
    .female {
      font-size: 12.5px;
      margin-left: 26px;
      margin-right: 43px;
    }
  }
  .names_image {
    width: 291px;
    height: 58px;
  }
  .invi_main_image {
    margin-top: 50px;
    width: 100%;
    height: auto;
  }
}
</style>