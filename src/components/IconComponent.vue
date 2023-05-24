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
    <div
    :id="`tooltip-no-arrow-${iconString}`"
    :role="tooltip"
      class="inline-block absolute invisible text-xs z-10 py-1 px-2 font-medium text-white rounded-sm shadow-sm opacity-0 tooltip dark:bg-gray-600 delay-150"
    >{{ text }}</div>
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
const { iconString, iconColor, hoverColor } = toRefs(props);
let icon = null;
if (iconString.value === "menu") {
  icon = menuIcon;
}
</script>
