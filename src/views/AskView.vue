<template>
  <list-item></list-item>
  <!-- <ul class="news-list">
    <li v-for="(item,idx) in this.$store.state.ask" :key="idx" class="post">
      <div class="points">
        {{item.points}}
      </div>
      <div>
        <p class="news-title">
          <router-link v-bind:to="`item/${item.id}`">
            {{item.title}}
          </router-link>
        </p>
        <small class="link-text">
          {{item.time_ago}}by
          <router-link v-bind:to="`/user/${item.user}`">{{item.user}}</router-link>
        </small>
      </div>
    </li>
  </ul> -->
</template>

<script>
import ListItem from '../components/ListItem.vue';
export default {
  components:{
    ListItem
  }
}
// import { /*mapState,*/ mapGetters } from 'vuex';
// export default {
//   computed:{
//     ...mapGetters([
//       'fetchedAsk'
//     ]),
//     // #2
//     // ...mapState({
//     //   fetchedAsk:state=>state.ask
//     // }),
//     // #1
//     // ask(){
//     //   return this.$store.state.ask;
//     // }
//   },
//   created(){
//     this.$store.dispatch('FETCH_ASK');
//     // fetchAskList()
//     //   .then(response=>this.ask=response.data)
//     //   .catch(error=>console.log(error))
//   }
// }
</script>

<style>


</style>