<template>
  <div class="form-group fixed-width mb-2">
    <label :for="fieldId" style="padding-right: 10px;">{{ label }}</label>
    <input type="text" :id="fieldName" class="form-control" :value="value" @input="updateValue($event.target.value)">
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    fieldName: String,
    value: String  // This is the value bound to the input
  },
  methods: {
    updateValue(newValue) {
      // Emit the input value to the parent component
      this.$emit('input', newValue);
    }
  }
};
</script>
