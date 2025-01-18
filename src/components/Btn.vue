<template>
  <div
      ref="navBtnRef"
      class="btn"
      @click="handleClick"
  >

    <slot/>
  </div>
</template>
<script setup lang="ts">
import {ref, watch} from 'vue';

interface IProps {
  isClicked?: boolean;
}

const props = withDefaults(defineProps<IProps>(), {
  isClicked: false,
});
const emit = defineEmits(['click', 'update:isClicked']);

const localIsClicked = ref(props.isClicked);

const navBtnRef = ref(null);

const handleClick = () => {
  localIsClicked.value = !localIsClicked.value;
  emit('update:isClicked', localIsClicked.value);
  emit('click');
};

watch(
    () => props.isClicked,
    (newValue) => {
      localIsClicked.value = newValue;
    },
);
</script>

<style lang="scss">

.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: fit-content;
  height: 42px;
  padding: 8px 12px;
  text-overflow: ellipsis;
  white-space: nowrap;
  cursor: pointer;
  user-select: none;
  border-radius: 8px;
  color: #fff;
  background: #2164E1;

  &:hover {
    background-color: #2a58b0;;
  }
}
</style>
