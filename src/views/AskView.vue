<template>
  <div>
    <div v-for="item in fetchedAsk" :key="item">{{ item.title }}</div>
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