<template>
  <div>
    <b-input-group>
      <b-form-tags
        class="bg-warning border-0 text-dark"
        tag-variant="dark"
        placeholder="Adicione tags"
        v-model="tags"
        @input="addTag"
      ></b-form-tags>
    </b-input-group>
  </div>
</template>

<script>
export default {
  name: "n-tag",
  props: {
    tags: [Array, String],
  },
  data() {
    return {};
  },
  methods: {
    async addTag() {
      this.$emit("addTag", this.tags);
    },
  },
};
</script>

<style>
</style>
