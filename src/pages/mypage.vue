<template>
  <vs-row vs-w="12" class="mypage">
    <vs-col vs-type="flex" vs-justify="center" vs-align="flex-start" vs-lg="3" vs-sm="3" vs-xs="12" >
      <vs-card style="text-align: center;padding-bottom: 32px;">
        <div>
          <vs-avatar /><br>
          <span>admin</span>
        </div>
      </vs-card>
    </vs-col>
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="1" vs-sm="1" vs-xs="12" />
    <vs-col vs-type="flex" vs-justify="center" style="flex-direction: column" vs-direction="column" vs-align="center" vs-lg="8" vs-sm="8" vs-xs="12">
      <router-link class="link" style="margin-bottom: 32px;flex: 1;width: 100%;display: block;" :to="`/posts/${number}`" v-for="number in 10" :key="number">
        <vs-card>
          <div slot="header">
            <h3>
              Hello world !
            </h3>
          </div>
          <div>
            <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
          </div>
          <div slot="footer">
            <vs-row vs-justify="flex-end">
              <FavoriteButton :isLiked="false" />
            </vs-row>
          </div>
        </vs-card>
      </router-link>
    </vs-col>
  </vs-row>
</template>

<script>
import FavoriteButton from '../components/FavoriteButton.vue'

export default {
  components: {
    FavoriteButton
  }
}
</script>

<style>
.mypage .vs-sidebar-background {
  display: none;
}
</style>
