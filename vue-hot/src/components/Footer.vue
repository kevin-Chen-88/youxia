<template>
  <div class="warp footer">
    <div class="sub-wrap">
      <div class="content">
        <p>Copyright © 普元信息技术股份有限公司保留所有权利 </p>
        <p>未经授权，严禁非法复制或镜像</p>
        <p>沪ICP备12006232号-2</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss">
.footer {
  background: #000;

  .content {
    color: #9b9b9b;
    padding: 20px 0;
    font-size: 14px;

    p {
      line-height: 26px;
    }
  }
}
</style>
