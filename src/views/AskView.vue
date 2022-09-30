<template>
<div>
  <div>
    <p v-for="(item,idx) in this.$store.state.ask" :key="idx">
      <!-- <a v-bind:href="item.url">
        {{ item.title }}
      </a> -->
      <router-link v-bind:to="`item/${item.id}`">
        {{item.title}}
      </router-link>
      <small>{{item.time_ago}}by{{item.user}}</small>
    </p>
  </div>
</div>
</template>

<script>
import { /*mapState,*/ mapGetters } from 'vuex';
export default {
  computed:{
    ...mapGetters([
      'fetchedAsk'
    ]),
    // #2
    // ...mapState({
    //   fetchedAsk:state=>state.ask
    // }),
    // #1
    // ask(){
    //   return this.$store.state.ask;
    // }
  },
  created(){
    this.$store.dispatch('FETCH_ASK');
    // fetchAskList()
    //   .then(response=>this.ask=response.data)
    //   .catch(error=>console.log(error))
  }
}
</script>

<style>

</style>