<template>
  <div>
    <list-item></list-item>
    <!-- <ul class="news-list">
      <li v-for="(job,idx) in this.$store.state.jobs" :key="idx" class="post">
        <div class="points">
          {{job.comments_count}}
        </div>
        <div>
          <p class="news-title">
            <a :href="job.url">{{job.title}}</a>
          </p>
          <small class="link-text">
            {{job.time_ago}}by
            <a :href="job.url">
              {{job.domain}}
            </a>
          </small>
        </div>
      </li>
    </ul> -->
  </div>
</template>


<script>
import ListItem from '../components/ListItem.vue';
export default {
  components:{
    ListItem
  }
}
</script>

<style>
  
</style>