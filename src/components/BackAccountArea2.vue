<template>
  <div class="bank_area">
      <div class="title_area _english_font _big_text _green">
        Celebrate
      </div>
    <div class="_big_text _green">
      <b>Tempat untuk menyampaikan perasaan Anda</b>
    </div>

    <div class="text_area _large_text _gray">
      Untuk Anda yang kesulitan hadir,<br>
      silakan sampaikan ucapan selamat Anda dengan memberikan sumbangan.<br>
      Meskipun tidak dengan sumbangan, kami sangat berterima kasih<br>
      hanya dengan adanya dukungan Anda.
    </div>

    <bank-accordion style="margin-top: 24px;padding-bottom: 5px"/>

  </div>
</template>

<script>
import BankAccordion from "@/components/BankAccordion.vue";

export default {
  name: "bank-account-area",
  components: {
    BankAccordion,
  },
  data() {
    return {
    };
  },
  mounted() {
  },
  methods: {
  }
};
</script>

<style lang="scss" scoped>

.bank_area {
  margin-top: 56px;
  padding-bottom: 56px;
  text-align: center;
  background: var(--secondary-bg-color);
}

.title_area {
  padding-top: 54px;
  line-height: 24px;
  margin-bottom: 8px;
}

.text_area {
  margin-top: 16px;
  line-height: 30px;
  letter-spacing: -0.2%;
}
</style>
