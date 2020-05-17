<template>
  <div id="father">
    <main class="main">
      <section>
        hello
        <contact> </contact>
        <education></education>
        <experience></experience>
        <personal></personal>
      </section>
    </main>
    <footer class="footer">
      <guide-footer @printPDF="printPDF" @printPNG="printPNG"></guide-footer>
    </footer>
  </div>
</template>

<script>
import contact from "@/components/contact";
import education from "@/components/education";
import experience from "@/components/experience";
import personal from "@/components/personal";
import guideFooter from "@/components/guideFooter";

export default {
  name: "Home",
  components: {
    contact,
    education,
    experience,
    personal,
    guideFooter
  },
  methods: {
    printPDF() {
      // 加入页面打印逻辑
      console.log('111PDF')
    },
    printPNG() {
      // 加入页面保存快照逻辑
      console.log('222PNG')
    },
  }
};
</script>

<style>
#father {
  display: flex;
}

.main {
    height: 1000px;
}

.footer {
  position: fixed;
  min-width: 100%;
  bottom: 0;
  left: 50%;
  transform: translate(-50%);
}
</style>
