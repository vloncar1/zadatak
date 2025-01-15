<template>
  <div>
    <q-banner v-if="showBanner" class="bg-primary text-white">
      <template v-slot:action>
        <q-btn label="Close" flat @click="showBanner = false" />
      </template>
      <div>
        <p>{{ bannerMessage }}</p>
      </div>
    </q-banner>

    <q-input v-model="bannerMessage" label="Change Banner Message" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      showBanner: true,
      
      bannerMessage: "qbanner."
    };
  }
};
</script>

