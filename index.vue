<template>
    <div class="qrcode" ref="qrCodeUrl"></div>
</template>

<script>
  import QRCode from 'qrcodejs2'
  export default {
    name: 'login',
    data() {
      return {}
    },
    methods: {
      createQrCode() {
        this.qrCode = new QRCode(this.$refs.qrCode, {
          text: 'Scan QRCode',
          width: 200,
          height: 200,
          colorDark: '#000000',
          correctLevel: QRCode.correctLevel.H
        },)
    },
  },
  mounted() {
    this.createQrCode();
  }
}
</script>