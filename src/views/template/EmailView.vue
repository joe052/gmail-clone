<template>
  <div id="EmailView" class="bg-gray-50 h-screen">
    <div class="flex items-center p-2">
      <div class="flex justify-center items-center px-3.5">
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
        <div class="w-full bg-gray-200 flex items-center p-1 px-2 rounded-lg"></div>
      </div>
    </div>
  </div>
</template>

<script setup>
import IconComponent from "@/components/IconComponent.vue";
</script>
