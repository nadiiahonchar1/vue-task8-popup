<template>
  <div class="container">
    <div class="card">
      <h3>A modal window will open here</h3>
      <button class="btn" @click="modal = true">Open modal</button>
      <teleport to="#modal">
        <app-modal v-if="modal" @close="modal = false"></app-modal>
      </teleport>
    </div>
  </div>
</template>

<script>
import AppModal from "./components/AppModal.vue";
export default {
  name: "App",
  components: { AppModal },
  data() {
    return {
      modal: false,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  background-color: rgb(255 255 0 / 30%);
}

.container {
  margin: 0 auto;
  width: 50vw;
}

.card {
  border: 1px solid rgb(87, 87, 199);
  border-radius: 10px;
  margin-bottom: 5px;
  padding: 5px 20px;
}

.btn {
  display: inline-block;
  min-width: 100px;
  padding: 5px;
  border-radius: 20px;
  background-color: transparent;
  border: 1px solid #2756a8ad;
  color: #2756a8ad;
  cursor: pointer;
}

.btn:hover {
  border: 1px solid #2756a8ad;
  background-color: #2756a8ad;
  color: white;
  border-color: #022950;
}
</style>
