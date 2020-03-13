<template>
  <div id="my-modal" class="modal">
    <div class="modal-content">
      <Header />
      <Body />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "./Header";
import Body from "./Body";
import Footer from "./Footer";

export default {
  name: "Modal",
  components: {
    Header,
    Body,
    Footer
  }
};
</script>


<style scoped>
body {
  font-family: Arial, Helvetica, sans-serif;
  background: #f4f4f4;
  font-size: 17px;
  line-height: 1.6;
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
}
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  margin: 10% auto;
  width: 60%;
  box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 7px 20px 0 rgba(0, 0, 0, 0.17);
  animation-name: modalopen;
  animation-duration: 1s;
}
@keyframes modalopen {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>