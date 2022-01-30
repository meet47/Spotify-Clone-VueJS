<template>
  <div class="w-full bg-darkest" style="height: 12vh">
    <div class="flex items-center justify-center pt-4">
      <fa icon="undo-alt" color="white" class="mx-2" />
      <fa icon="step-backward" color="white" class="mx-2" />
      <fa icon="play-circle" color="white" size="3x" class="mx-2" />
      <fa icon="step-forward" color="white" class="mx-2" />
      <fa icon="redo-alt" color="white" class="mx-2" />
    </div>
    <div class="flex items-center justify-center mt-2">
      <img src="../assets/playbar.png" class="w-96 h-15" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>
