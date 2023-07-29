<template>
  <h2>{{ title }}</h2>
  <allFriends :friends="friends" @delete="deleteFriend" ></allFriends>
  <onlineFriends :friends="friends"></onlineFriends>
</template>

<script>
import allFriends  from "./components/AllFriends.vue";
import onlineFriends  from "./components/OnlineFriends.vue";

export default {
  name: 'App',
  data(){
    return{
      title:"Hurry! Our vue apps is running :)",
      friends:[
                { name:'A',online:true },
                { name:'B',online:true },
                { name:'C',online:false },
                { name:'D',online:true },
                { name:'E',online:false },
            ]
    }
  },
  components:{
    allFriends,onlineFriends
  },
  methods:{
    deleteFriend(payload){
      // console.log(payload);
      this.friends = this.friends.filter(friend =>{
        return friend.name !== payload.name;
      });
    }
  }
}
</script>

<style>
h2{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f71591;
  margin-top: 60px;
}
</style>
