<script>
export default {
  props: {
    showed: {
      type: Boolean,
      required: true,
    },
  },
  methods:{
      close(){
          this.$emit("close");
      }
  }
};
</script>
<template>
  <div v-if="showed" class="modal show" tabindex="-1">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Modal title</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
            @click="close()"
          ></button>
        </div>
        <div class="modal-body">
          <p>Modal body text goes here.</p>
        </div>
        <div class="modal-footer">
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
            @click="close()"
          >
            Close
          </button>
          <button type="button" class="btn btn-primary">Save changes</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.modal-window {
  position: fixed;
  width: 300px;
  left: calc(50%-150px);
  top: 50px;
  background-color: blue;
}
</style>