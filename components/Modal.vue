<template>
  <transition name="modal">
    <div class="modal-vue-mask">
      <div class="modal-vue-wrapper">
        <div class="modal-vue-container">

          <div class="modal-vue-header">
            <h3>Замовити</h3>
          </div>

          <div class="modal-vue-body">
            <v-form v-model="valid">
              <v-text-field v-model="name" :rules="nameRules" :counter="10" label="Name" required></v-text-field>
              <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
            </v-form>
          </div>

          <div class="modal-vue-footer">
            <slot name="footer">
              default footer
              <button class="modal-vue-default-button" @click="$emit('close')">
                OK
              </button>
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'modal',
  data: () => ({
    valid: false,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 10 || 'Name must be less than 10 characters'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v =>
        /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) ||
        'E-mail must be valid'
    ]
  })
}
</script>

<style lang="scss">
.modal-vue-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-vue-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-vue-container {
  width: 300px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-vue-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-vue-body {
  margin: 20px 0;
}

.modal-vue-default-button {
  float: right;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-vue-enter {
  opacity: 0;
}

.modal-vue-leave-active {
  opacity: 0;
}

.modal-vue-enter .modal-vue-container,
.modal-vue-leave-active .modal-vue-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>

