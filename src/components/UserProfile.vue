<template>
      <!-- 질문 상세 정보 -->
      <div class="user-container">
        <div>
          <i class="fa-solid fa-user"></i>
        </div>
        <div class="user-description">
          <div>{{info.id}}</div>
          <!-- <router-link :to="`/user/${userInfo.user}`">
            {{userInfo.id}}
          </router-link> -->
          <div class="time">
            {{info.created}}
          </div>
        </div>
      </div>
    <!-- <p>{{fatchedItem.title}}</p>
    <div>
      {{fatchedItem.content}}
    </div> -->
</template>

<script>
export default {
  props:{
    info:Object
  },
  // computed:{
  //   userInfo(){
  //     return this.$store.state.user;
  //   }
  // },
}
</script>

<style scoped>
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