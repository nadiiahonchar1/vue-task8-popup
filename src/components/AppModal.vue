<template>
  <div class="modal-backdrop" @click="$emit('close')">
    <div class="modal">
      <h3>This is the name of the modal</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa quis
        excepturi architecto tempore ipsam dolore fugiat voluptatibus aperiam!
        Quidem, corporis.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  emits: ["close"],
};
</script>

<style scoped>
.modal {
  position: fixed;
  top: 60px;
  width: 600px;
  padding: 1rem;
  background: #fff;
  z-index: 1000;
  left: 50%;
  border-radius: 10px;
  transform: translateX(-50%);
  box-shadow: 2px 3px 10px rgba(0, 0, 0, 0.2);
}

.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.35);
}
</style>
