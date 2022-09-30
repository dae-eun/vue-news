<template>
  <div>
    <section>
      <!-- 질문 상세 정보 -->
      <div class="user-container">
        <div>
          <i class="fa-solid fa-user"></i>
        </div>
        <div class="user-description">
          <router-link :to="`/user/${this.$store.state.item.user}`">
            {{this.$store.state.item.user}}
          </router-link>
          <div class="time">
            {{this.$store.state.item.time_ago}}
          </div>
        </div>
      </div>
      <h2>{{this.$store.state.item.title}}</h2>
    </section>
    <section>
      <!-- 질문 댓글 -->
      <div v-html="this.$store.state.item.content">

      </div>
    </section>
    <!-- <p>{{fatchedItem.title}}</p>
    <div>
      {{fatchedItem.content}}
    </div> -->
  </div>
</template>

<script>
import {mapGetters} from 'vuex';
export default {
  computed:{
    ...mapGetters(['fatchedItem']),
  },
  created(){
    const itemId = this.$route.params.id;
    this.$store.dispatch('FETCH_ITEM',itemId);
  }
}
</script>

<style>
.user-container{
  display:flex;
  align-items: center;
  padding:0.5rem;
}
.fa-user{
  font-size:2.5rem;
}
.user-description{
  padding-left:8px;
}
.time{
  font-size:7px;
}
</style>