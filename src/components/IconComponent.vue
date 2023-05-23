<template>
  <div id="IconComponent" class="hello">
    <div
      class="flex items-center justify-center rounded-full cursor-pointer w-10 h-10"
    >
      <component :is="icon" :size="iconSize" :fillColor="iconColor" />
    </div>
  </div>
</template>

<script setup>
import { toRefs, defineProps } from "vue";
import menuIcon from "vue-material-design-icons/Menu.vue";
const props = defineProps({
  iconString: String,
  iconColor: String,
  iconSize: String,
});
const { iconString, iconColor } = toRefs(props);
let icon = null;
if (iconString.value === "menu") {
  icon = menuIcon;
}
</script>
