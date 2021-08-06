<template>
  <div class="human">
    <div class="atama">
      <div v-if="isLaughing">🤣</div>
      <div v-else>{{ person.face }}</div>
    </div>
    <div class="karada" v-on:click="makeLaugh">
      <div>💪{{ person.cloth }}💪</div>
    </div>
    <div class="ashi">
      <div>🦵🦵</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    person: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      isLaughing: false,
    }
  },
  methods: {
    makeLaugh() {
      this.isLaughing = true
    },
  },
}
</script>

<style>
.human {
  width: 10rem;
  font-size: 3rem;
  text-align: center;
  white-space: nowrap;
}
</style>