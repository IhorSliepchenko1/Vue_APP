<template>
  <label class="chk" @click="toggleCheckbox">
    <input type="checkbox" v-model="isChecked" />
    <span class="chk__block">
      <CheckmarkIcon v-if="isChecked" />
    </span>
    <span v-if="label">{{ label }}</span>
  </label>
</template>
  
<script>
import CheckmarkIcon from "./../../icons/CheckmarkIcon.vue";

export default {
  components: {
    CheckmarkIcon
  },
  props: {
    label: String
  },
  data() {
    return {
      isChecked: false
    };
  },
  methods: {
    toggleCheckbox() {
      this.isChecked == !this.isChecked;
    }
  }
};

console.log()
</script>
  
<style scoped lang="scss">
.chk {
  display: inline-flex;
  gap: 8px;
  align-items: center;
  cursor: pointer;

  span {
    color: #344054;
    font-family: Inter;
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
  }

  input {
    display: none;
  }

  input:checked~.chk__block {
    background: #5429ff;
    border-color: #5429ff;

    svg {
      transform: scale(1);
    }
  }

  &__block {
    border-radius: 4px;
    border: 1px solid #d0d5dd;
    width: 16px;
    height: 16px;
    transition: 0.2s all ease-in-out;

    svg {
      transform: scale(0);
      width: 14px;
      height: 14px;
      transition: 0.2s all ease-in-out;
    }
  }
}
</style>
  