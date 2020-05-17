<template>
  <div class="guide-footer">
    <div>
      <span>操作</span>
    </div>

    <ul>
      <li>
        <img src="../assets/guide_click_left.png" width="40" alt="鼠标左键" >
        <div class="desc">
          <strong>左键点击</strong>
          <p>编辑文本内容或更改图片</p>
        </div>
      </li>
      <li>
        <img src="../assets/guide_click_right.png" width="40" alt="鼠标右键" >
        <div class="desc">
          <strong>右键点击</strong>
          <p>删除项目</p>
        </div>
      </li>
    </ul>
    <button @click="print">打印</button>
    <button @click="printPNG">保存为PNG</button>
  </div>
</template>

<script>
export default {
  name: 'Guide',
  methods: {
    print() {
      this.$emit('printPDF')
    },
    printPNG() {
      this.$emit('printPNG')
    }
  }
}
</script>

<style scoped>
.guide-footer {
  display: flex;
  padding: 2px 10px;
  justify-content: center;
  align-items: center;
}

ul {
  display: flex;
  list-style: none;
}

span {
  font-size: 1.2em;
  font-weight: bold;
}

li {
  display: flex;
  margin: 0 3px;
}

button {
  font-size: 1em;
  padding: 5px;
  border-radius: 4px;
  background-color: white;
  border: 1px solid #dad8d7;
  margin: 5px 3px;
  cursor: pointer;
}

button:hover {
  background-color: #f8f8f8;
}
</style>
