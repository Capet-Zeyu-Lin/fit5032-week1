<script setup>
defineProps({
  userName: {
    type: String,
    required: true,
  },
})
</script>

<template>
    <h1 class="typing">Et tu,{{userName}}?</h1>
</template>

<style>

h1 {
  color: white;
  font-size: 2rem;
  text-align: center;
  font: times new roman;
  background: linear-gradient(to right, #00f260, #0575e6);
  -webkit-background-clip: text;
  color: transparent;
}

.typing {
  overflow: hidden;
  white-space: nowrap;
  border-right: 3px solid #fff;
  animation: typing 3s steps(30, end), blink 0.75s step-end infinite;
}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}
@keyframes blink {
  50% { border-color: transparent }
}

</style>