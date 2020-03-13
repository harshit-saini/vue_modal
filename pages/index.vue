<template>
  <div class="container">
    <button id="modal-btn" class="button" @click="openModal">Click Here</button>

    <Modal />
  </div>
</template>


<script>
import Modal from "../components/Modal";

export default {
  components: {
    Modal
  },
  methods: {
    openModal: function() {
      console.log("clicked");
      const modal = document.getElementById("my-modal");

      document.getElementById("modal-btn").addEventListener("click", () => {
        modal.style.display = "block";
      });
    }
  }
};
</script>

<style scoped >
.container {
  display: flex;
  justify-content: center;
  margin-top: 40px;
}
.button {
  background: #428bca;
  padding: 1em 2em;
  color: #fff;
  border: 0;
  border-radius: 5px;
  cursor: pointer;
}

.button:hover {
  background: #3876ac;
}
</style>





