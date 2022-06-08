<template>
  <div id="navcrx" style="position: relative;">

    <div
      :style="{
        width: '120px',
        height: '50px',
        lineHeight: '50px',
        borderColor: '#6777ef',
        cursor: 'pointer',
        fontSize: '20px'
      }"
      @click="handleClick"
      class="crx-btn"
      v-show="!visible"
    >
      程序员导航
    </div>

    <a-drawer title="程序员导航" :width="500" :visible="visible" @ok="handleOk" @cancel="handleCancel" unmountOnClose :footer="false">

    <iframe style="border: none" width="100%" height="100%" src="https://luo0412.github.io/idx"></iframe>

  </a-drawer>
</div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "App",
  setup() {
    const visible = ref(false);

    const handleClick = () => {
      visible.value = true;
    };
    const handleOk = () => {
      visible.value = false;
    };
    const handleCancel = () => {
      visible.value = false;
    }

    return {
      visible,
      handleClick,
      handleOk,
      handleCancel,
    }
  }
});
</script>

<style lang="less" scoped>
@import "../style/popup.less";
</style>

<style lang="less">
#navcrx {
.arco-drawer-body {
  padding: 0;
  overflow-y: hidden;
}

.arco-drawer-header {
  display: none;
}
}

</style>


