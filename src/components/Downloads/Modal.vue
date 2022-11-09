<template>
  <div class="modal" :class="[canShowModal ? 'show' : 'hide']">
    <div v-for="(item, index) in items" :key="index" class="modal-flex-row">
      <div class="modal-icon-col">
        <Icon class="modal-icon" />
      </div>
      <div class="modal-text-col">
        <p class="modal-text">{{ item.title }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import Icon from "@/components/Icons/Icon.vue";
export default {
  props: {
    canShowModal: Boolean,
    items: Array,
  },
  components: {
    Icon,
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
  background-color: #ffffff;
  border-radius: 5px;
}

.modal-flex-row + .modal-flex-row {
  border-top: 1px solid #d8d9db80;
}

.modal-flex-row {
  display: flex;
  height: 56px;
  border-radius: 5px;
  // NB: Primary Red
  &:hover {
    color: #ff1f27;
    .modal-icon {
      stroke: #ff1f27;
    }
  }
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
  // NB: Transparencies/Grey Light 50%
  border-right: 1px solid #d8d9db80;
}

.modal-icon {
  // NB: Primary Blue
  stroke: #1b1464;
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
