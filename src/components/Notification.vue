<template>
  <div class="notification"></div>
</template>
<script>
export default {
  name: "Notification",
  props: {
    type: Number,
    content: Object
  },
  computed: {
    typeData() {
      let r;

      switch (this.type) {
        case 0: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 1: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 2: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 3: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 4: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 5: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
        case 6: {
          r = {
            typeName: "",
            icon: ""
          };
          break;
        }
      }

      return r;
    }
  }
};
</script>
<style lang="scss">
.notification {
  height: calc(var(--scale) * 8vh);
  width: calc(var(--scale) * 32vh);
  border: 1px solid red;
}
</style>
