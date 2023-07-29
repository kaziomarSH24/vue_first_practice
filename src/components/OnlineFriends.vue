<template>
    <div id="onlineFriends">
        <h1>Online Friends</h1>
        <div v-for="(friend,index) in friends" :key="index">
            <h6 v-if="friend.online">{{ friend.name }}</h6>
        </div>
    </div>
</template>

<script>
export default {
    name:'onlineFriends',
    props:['friends'],
    data(){
        return{
            
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
  color: #2ff715;
  margin-top: 60px;
}
</style>
