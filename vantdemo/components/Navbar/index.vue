<template>
    <!-- 固定定位，左侧箭头，标题，右侧文字 -->
    <van-nav-bar
      fixed
      left-arrow
      @click-left="onClickLeft"
      :title="title"
      :right-text="rightText"
      @click-right="onClickRight"
    ></van-nav-bar>
</template>
  