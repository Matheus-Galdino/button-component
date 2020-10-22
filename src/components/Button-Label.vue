<template>
  <label> &lt;{{ content }} /&gt; </label>
</template>

<script>
export default {
  name: "Button-Label",
  props: {
    content: String,
  },
};
</script>

<style>
label {
  font-family: "Ubuntu Mono", monospace;
  font-size: 14px;
  line-height: 12px;

  color: #333333;
}
</style>