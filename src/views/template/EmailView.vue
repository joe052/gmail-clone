<template>
  <div id="EmailView" class="bg-gray-50 h-screen">
    <div class="flex items-center p-2">
      <div class="logo-section flex justify-center items-center px-3.5">
        <IconComponent
          iconString="menu"
          iconColor="#636363"
          :iconSize="19"
          hoverColor="hover:bg-gray-200"
          text="Main Menu"
          class="-ml-2 mr-2"
        />

        <img width="107" src="../../../public/img/gmail.png" alt="" />
      </div>
      <div class="flex w-full justify-between">
        <div class="w-full bg-gray-200 flex items-center p-1 px-2 rounded-lg">
          <IconComponent
            iconString="magnify"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="Search"
          />
          <input
            placeholder="Search mail"
            class="w-full h-10 bg-gray-200 border-transparent border-none focus:ring-0 outline-none placeholder-gray-900"
            type="text"
          />
          <IconComponent
            iconString="tune"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="Show search options"
          />
        </div>
        <div class="flex w-32 justify-between items-center ml-6">
          <IconComponent
            iconString="cog"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="Settings"
          />
          <IconComponent
            iconString="apps"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="Google apps"
          />
          <UserComponent />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import IconComponent from "@/components/IconComponent.vue";
import UserComponent from "@/components/UserComponent.vue";
</script>

<style lang="scss">
#EmailView {
  .logo-section {
    min-width: 250px;
  }
}
</style>
