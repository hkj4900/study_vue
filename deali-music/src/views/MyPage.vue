<template>
  <div class="myPage_container">
    <h2>
      My Page
    </h2>
    <h3>
      <router-link to='/myMusic'>내 음악</router-link>
    </h3>
    <h5>
      {{ userName }}님 안녕하세요.
    </h5>
    <MusicRegist></MusicRegist>
    <MusicList></MusicList>
  </div>
</template>

<script>
import MusicList from '../components/MyPage/MusicList';
import MusicRegist from '../components/MyPage/MusicRegist';

export default {
  name: 'MyPage',
  components: {
    MusicList,
    MusicRegist,
  },
  data(){
    return {
      userName: this.$store.state.userName,
    }
  },
}
</script>
<style lang="scss" scoped>
  .myPage_container{
    text-align: center;
  }
</style>
