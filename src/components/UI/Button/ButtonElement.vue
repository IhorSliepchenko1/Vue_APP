<template>
    <button :class="className">
        <slot></slot>
    </button>
</template>
  
<script>
export default {
    props: {
        className: String
    }
};
</script>
  
<style scoped lang="scss">
.btn {
    display: inline-flex;
    width: 100%;
    bottom: 0;
    outline: 0;
    cursor: pointer;
    border-radius: 8px;
    justify-content: center;
    align-items: center;

    &._primary {
        background: #5429ff;
        color: #fff;
        font-family: Inter;
        font-size: 16px;
        font-weight: 500;
        line-height: 20px;
        border: 0;
        padding: 12px 154px;
    }

    &._secondary {
        border: 1px solid #d0d5dd;
        color: #344054;
        font-family: Inter;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: 20px;
        background: transparent;
        padding: 10px 90px;
    }
}
</style>
  