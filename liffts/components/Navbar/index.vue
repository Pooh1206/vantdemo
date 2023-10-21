<template>
    <van-nav-bar
      fixed
      left-arrow
      @click-left="onClickLeft"
      :title="title"
      :right-text="rightText"
      @click-right="onClickRight"
    ></van-nav-bar>
</template>

<style lang="scss" scoped>
:deep() {
  .van-nav-bar {
    &__arrow {
      color: var(--cp-text1);
      font-size: 18px;
    }
    &__title {
      font-size: 15px;
    }
  }
}
</style>