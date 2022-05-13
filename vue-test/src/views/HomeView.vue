<template>
  <div class="homeView">
    <h1>HOME</h1>
    <div class="user-list">
      <router-link v-for="user in users" :to="{name: 'UserProfile', params: {userId: user.id }}" :key="user.id">
      {{ user.username }}
      </router-link>

    </div>
  </div>
</template>

<script>
import {users} from "../assets/users";
export default{
  name: "Home-View",
  setup(){
    return{
      users
    }
  }
}
</script>

<style lang="scss" scoped>
.user-list{
  display: flex;
  flex-direction: column ;
}
</style>