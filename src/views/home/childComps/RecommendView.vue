!<template>
  <div class="recommend">
    <div v-for="item in recommends" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    recommends:{
      type:Array,
      default(){
        return[]
      }
    }
  }

}
</script>

<style>
.recommend{
  display: flex;
  font-size: 14px;
  text-align: center;
  padding: 10px 0 20px;
  border-bottom: 8px solid #eee;
}
.recommend-item{
  flex: 1;
  margin-bottom: 10px;
  

}
.recommend-item img{
 width: 100px;
 height: 100px;
}

</style>