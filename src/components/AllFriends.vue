<template>
    <div id="allFriends">
        <h1>All Friends</h1>
        <div v-for="(friend,index) in friends" :key="index">
            <h6 @click="unfriend(friend.name)">{{ friend.name }}</h6>
        </div>
    </div>
</template>

<script>
export default {
    name:'allFriends',
    props:['friends'],
    data(){
        return{
            
        }
    },
    methods:{
        unfriend(name){
            // console.log(name);
           this.$emit('delete',{name});
        }
    }
    
}
</script>

<style scoped>
h1{
    text-align: center;
}
    h6{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f71591;
  margin-top: 60px;
}
</style>
