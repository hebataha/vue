<template>
  <div>
    <div>
      <b-input-group prepend="$" append=".00">
        <b-form-input></b-form-input>
      </b-input-group>

      <b-input-group prepend="0" append="100" class="mt-3">
        <b-form-input type="range" min="0" max="100"></b-form-input>
      </b-input-group>
    </div>

    <div>
      <b-form-timepicker v-model="value" locale="en"></b-form-timepicker>
      <div class="mt-2">Value: '{{ value }}'</div>
    </div>
    <div>
      <b-table striped hover :items="items"></b-table>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: "",
      items: [
        { age: 40, first_name: "Dickerson", last_name: "Macdonald" },
        { age: 21, first_name: "Larsen", last_name: "Shaw" },
        { age: 89, first_name: "Geneva", last_name: "Wilson" },
        { age: 38, first_name: "Jami", last_name: "Carney" },
      ],
    };
  },
};
</script>

<style></style>
