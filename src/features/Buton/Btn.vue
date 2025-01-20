<template>
  <div ref="navBtnRef" class="btn" :class="colors" @click="handleClick">
    <slot />
  </div>
</template>
<script setup lang="ts">
import { computed, ref, watch } from "vue";

interface IProps {
  isClicked?: boolean;
  type?: "primary" | "secondary";
}

const props = withDefaults(defineProps<IProps>(), {
  isClicked: false,
  type: "primary",
});
const emit = defineEmits(["click", "update:isClicked"]);

const localIsClicked = ref(props.isClicked);

const navBtnRef = ref(null);

const handleClick = () => {
  localIsClicked.value = !localIsClicked.value;
  emit("update:isClicked", localIsClicked.value);
  emit("click");
};

watch(
  () => props.isClicked,
  (newValue) => {
    localIsClicked.value = newValue;
  },
);

const colors = computed(() => {
  if (props.type === "secondary") {
    return "btn-secondary";
  }
});
</script>

<style lang="scss">
.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: fit-content;
  height: 42px;
  padding: 10px 16px;
  text-overflow: ellipsis;
  white-space: nowrap;
  cursor: pointer;
  user-select: none;
  border-radius: 8px;
  color: #fff;
  background: #2164e1;

  &:hover {
    background-color: #2a58b0;
  }
}

.btn-secondary {
  background: #30b467;

  &:hover {
    background-color: #2d9638;
  }
}
</style>
