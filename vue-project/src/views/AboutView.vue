<script>
import Modal from "../components/Modal.vue";
export default {
  components: {
    Modal,
  },
  data: () => {
    return {
      modalShowed: false,
    };
  },
  methods: {
    showModal(){
      this.modalShowed = true;
    },
    hideModal(){
      this.modalShowed = false;
    }
  }
};
</script>
<template>
  <div>
    <h1>This is an about page</h1>
    <section>
      <Modal :showed="modalShowed" @close="hideModal()"/>
      <button @click="showModal()">Modal window</button>
    </section>
  </div>
</template>

<style>
</style>
