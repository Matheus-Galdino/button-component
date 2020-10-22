<template>
  <button
    :class="[
      size,
      variant,
      color,
      { 'disable-shadow': disableShadow, disabled: disabled },
    ]"
    :disabled="{ disabled }"
  >
    <span class="material-icons" v-if="startIcon"> {{ startIcon }} </span>
    <p v-if="disabled">Disabled</p>
    <p v-else>{{ showContent }}</p>
    <span class="material-icons" v-if="endIcon"> {{ endIcon }} </span>
  </button>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    content: {
      type: String,
      default: "Default",
    },
    size: {
      type: String,
      default: "md",
      validator: function (value) {
        return ["sm", "md", "lg"].indexOf(value) !== -1;
      },
    },
    variant: {
      type: String,
      default: "",
      validator: function (value) {
        return ["", "outline", "text"].indexOf(value) !== -1;
      },
    },
    color: {
      type: String,
      default: "default",
      validator: function (value) {
        return (
          ["default", "primary", "secondary", "danger"].indexOf(value) !== -1
        );
      },
    },
    startIcon: String,
    endIcon: String,
    disabled: { type: Boolean, default: false },
    disableShadow: Boolean,
  },
  computed: {
    showContent() {
      return this.content !== "Default" ? this.content : this.color;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  display: flex;
  align-items: center;

  background: #e0e0e0;
  box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
  border-radius: 6px;
  border: none;

  margin-top: 10px;

  font-family: "Noto Sans JP", sans-serif;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;

  color: #3f3f3f;
  cursor: pointer;

  transition: all 0.2s ease-out;
}

button:hover {
  background: #aeaeae;
}

button p {
  margin: 0 8px;
}

button p:first-letter {
  text-transform: capitalize;
}

/*#region variants */

.outline {
  border: 1px solid #3d5afe;
  background: none;

  color: #3d5afe;
}

.text {
  background: transparent;
  border: none;
  box-shadow: none;
  color: #3d5afe;
}

.outline:hover,
.text:hover {
  background: rgba(41, 98, 255, 0.1);
}

/*#endregion*/

/*#region Disableds */
.disable-shadow {
  background: #3d5afe;
  box-shadow: none;
  color: white;
}

.disable-shadow:hover {
  background: #3d5afe;
  box-shadow: none;
  color: white;
}

.disabled {
  color: #9e9e9e;
}

.disabled:hover {
  background: #e0e0e0;
}
/*#endregion */

/*#region sizes */
.sm {
  padding: 6px 12px;
}

.md {
  padding: 8px 16px;
}

.lg {
  padding: 11px 22px;
}
/*#endregion */

/*#region Colors */
/* .default{

} */

.primary,
.secondary,
.danger {
  color: white;
}

.primary {
  background: #2962ff;
  box-shadow: 0px 2px 3px rgba(41, 98, 255, 0.2);
}

.primary:hover {
  background: #0039cb;
}

.secondary {
  background: #455a64;
  box-shadow: 0px 2px 3px rgba(69, 90, 100, 0.2);
}

.secondary:hover {
  background: #1c313a;
}

.danger {
  background: #d32f2f;
  box-shadow: 0px 2px 3px rgba(211, 47, 47, 0.2);
}

.danger:hover {
  background: #9a0007;
}

/*#endregion */
</style>
