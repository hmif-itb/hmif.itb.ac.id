<template>
  <div class="perimeter pa-2 fill-height" align="center">
    <!--<div align="center">-->
      <!--<v-img :src="image" :aspect-ratio="1" class="img" />-->
    <!--</div>-->
    <div class="font-weight-bold">
      <small>{{ name }}</small>
    </div>
    <div>
      <small>{{ title }}</small>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamProfile",
  props: ['name', 'title']
}
</script>

<style scoped>
  .perimeter {
    border: 2px dashed #FF9800;
    border-radius: 8px;
  }

  .img {
    width: 80px;
    border-radius: 8px;
  }
</style>
