<template>
  <div class="modal-header">
    <span class="close" @click="closeModal">&times;</span>
    <h2>Modal Header</h2>
  </div>
</template>

<script>
export default {
  methods: {
    closeModal: function() {
      const modal = document.getElementById("my-modal");

      document.querySelector(".close").addEventListener("click", () => {
        modal.style.display = "none";
      });
    }
  }
};
</script>

<style scoped>
.modal-header h2,
.modal-footer h3 {
  margin: 0;
}

.modal-header {
  background: #428bca;
  padding: 15px;
  color: #fff;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
.close {
  color: #ccc;
  float: right;
  font-size: 30px;
  color: #fff;
}

.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
}
</style>