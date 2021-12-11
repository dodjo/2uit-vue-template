<template>
  <div
      class="sidebar"
      :data="backgroundColor">
      <div class="sidebar-wrapper text-left">
        <div class="logo">
          <a href="javascript:void(0)" class="simple-text logo-normal">
            <img src="https://thumb.tildacdn.com/tild6633-3965-4661-b635-643135383232/-/resize/250x/-/format/webp/logo_2uit_opacity_25.png" />
          </a>
        </div>
        <ul class="nav">
          <slot>
            <sidebar-link>
            </sidebar-link>
          </slot>
        </ul>
      </div>
  </div>
</template>
<script>
import SidebarLink from "./SidebarLink.vue";

export default{
  name: "side-bar",
  components: {
    SidebarLink
  },
  props: {
    backgroundColor: {
      type: String,
      default: "green"
    },
    sidebarLinks:{
      type: Array,
      default: () => []
    }
  },
  data(){
    return{
      activeLinkIndex: 0
    }
  },
  methods:{
    findActiveLink(){
      this.links.forEach((link, index) => {
        if(link.isActive()){
          this.activeLinkIndex = index;
        }
      });
    }
  }
}
</script>
<style>
</style>
