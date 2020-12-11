<template>
  <div class="recommand">
    <div v-for="(item, id) in recommends" :key="id" class="recommand-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "RecommandView",
    props: {
      recommends: {
        type: Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
  .recommand {
    display: flex;
    text-align: center;
    font-size: 12px;

    padding: 10px 0 10px;

    border-bottom: 10px solid #eee;
  }

  .recommand-item {
    flex: 1;
  }

  .recommand img {
    width: 70px;
    height: 70px;
    margin-bottom: 10px;
  }
</style>
