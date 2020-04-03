<template>
  <div class="dummy-nav">
    <div class="title">
      <div class="logo">
        <object class="svg" :data="logoSvg"></object>
      </div><div class="heading">
        <h1>Animal Crossing Pattern Tool</h1>
        <h2>Compatible with Animal Crossing: New Leaf, Animal Crossing: Happy Home Designer and Animal Crossing: New Horizons</h2>
        <h2>By Thulinma, DamSenViet, Myumi, OneKintaro and Swordi</h2>
        <h2>Powered by <a href="https://acnh.ch" target="_blank">acnh.ch</a></h2>
      </div>
    </div>
    <div class="button browse" @click="goToBrowse">
      <div class="text">Browse</div>
    </div>
    <div class="button editor" @click="goToEditor">
      <div class="text">Editor</div>
    </div>
    <div class="button discord">
      <a href="https://discord.gg/FbDTwPN" class="text">ACNH.ch Discord</a>
    </div>
  </div>
</template>

<script>
import logoSvg from '/assets/images/discord_icon_demoto_rot.png';
export default {
  name: "Home",
  data: function(){
    return {logoSvg};
  },
  methods: {
    goToBrowse: function() {
      this.$router.push({ path: `/browse` });
    },
    goToEditor: function() {
      this.$router.push({ path: `/editor` });
    },
    goToFAQ: function() {
      this.$router.push({ path: `/faq` });
    },
    goToChanges: function() {
      this.$router.push({ path: `/changelog` });
    },
  }
}
</script>

<style lang="scss" scoped>

.title .logo{
  float:left;
}
.title{
  min-height:380px;
}
h1{
  font-size:80px;
}

.dummy-nav {
  font-family: Nunito;
}

.button {
  position: relative;
  cursor: pointer;
  padding:10px;
  box-sizing: border-box;
  color: white;
}

.button.browse {background-color: rgb(52, 171, 109);}
.button.editor {background-color: #1083cd;}
.button.faq {background-color: #f16060;}
.button.changelog {background-color: #cdb610;}
.button.discord {background-color: #7289da;}

.text {
  font-size: 2rem;
  color:#fff;
  text-decoration:none;
}
</style>
