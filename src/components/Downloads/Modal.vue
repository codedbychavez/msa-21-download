<template>
  <div class="modal" :class="[canShowModal ? 'show' : 'hide']">
    <div v-for="(item, index) in items" :key="index" class="modal-flex-row">
      <div class="modal-icon-col">
        <a href="#" target="_blank">
          <img src="@/assets/images/icon.svg" />
        </a>
      </div>
      <div class="modal-text-col">
        <p class="modal-text">{{ item.title }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    canShowModal: Boolean,
    items: Array,
  },
};
</script>

<style lang="scss">
.hide {
  display: none;
}

.show {
  display: block;
}

.modal {
  width: 280px;
  box-shadow: 0px 20px 24px -4px rgba(16, 24, 40, 0.08),
    0px 8px 8px -4px rgba(16, 24, 40, 0.03);
  background-color: #FFFFFF;
  border-radius: 5px;
}

.modal-flex-row + .modal-flex-row {
  border-top: 1px solid #d8d9db80;
}

.modal-flex-row {
  display: flex;
  height: 56px;
  border-radius: 5px;
}

.modal-icon-col,
.modal-text-col {
  display: flex;
  justify-content: center;
  align-items: center;
  // NB: Adjust the padding as needed
  padding: 16px;
}

.modal-icon-col {
  width: 56px;
  border-right: 1px solid #d8d9db80;
}

.modal-text-col {
  width: 100%;
  margin: 0 auto;
}

@media (min-width: 600px) {
  .modal {
    width: 644px;
  }

  .modal-text-col {
    justify-content: flex-start;
    padding-left: 24px;
  }

  .modal-icon-col {
    width: 72px;
  }
}
</style>
