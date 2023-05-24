<template>
  <div id="IconComponent" class="hello">
    <div
      class="flex items-center justify-center rounded-full cursor-pointer w-10 h-10"
      :class="[hoverColor]"
      :data-tooltip-target="`tooltip-no-arrow-${iconString}`"
      data-tooltip-placement="bottom"
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
  iconSize: Number,
  text: String,
  hoverColor: String,
});
const { iconString, iconColor, text, hoverColor } = toRefs(props);
let icon = null;
if (iconString.value === "menu") {
  icon = menuIcon;
}
</script>
