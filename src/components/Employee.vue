<template>
  <div>
    <input v-model="newName" placeholder="Enter name" />
    <input v-model="newSurn" placeholder="Enter surname" />
    <button @click="save">save</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newName: '',
      newSurn: '',
    };
  },
  methods: {
    save() {
      if (this.newName && this.newSurn) {
        this.$emit('add', this.newName, this.newSurn);
        this.newName = '';
        this.newSurn = '';
      }
    },
  },
};
</script>
