<template>
  <v-container>
    <v-card class="mx-auto my-12" max-width="800" outlined>
      <v-img v-if="url" :src="url" class="my-3" contain height="200" />
      <v-img
        v-else
        :src="require('../assets/layers.png')"
        class="my-3"
        contain
        height="200"
      />
      <v-file-input
        type="file"
        @change="onFileChange"
        class="mx-12"
        accept="image/png, image/jpeg, image/bmp"
        placeholder="Faça o upload da imagem desejada"
        prepend-icon="mdi-camera"
      ></v-file-input>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "UploadImage",

  data: () => ({
    url: null,
  }),
  methods: {
    onFileChange(e) {
      const file = e;
      if (file) {
        this.url = URL.createObjectURL(file);
        URL.revokeObjectURL(file);
      } else {
        this.url = null;
      }
    },
  },
};
</script>
