<template>
  <div class="deck-footer" aria-hidden="true">
    <span>{{ $nav.currentPage }} / {{ $nav.total }}</span>
  </div>
</template>

<style scoped>
.deck-footer {
  position: absolute;
  bottom: 12px;
  left: 60px;
  right: 60px;
  display: flex;
  justify-content: flex-end;
  color: #466179;
  font: 10px Arial, sans-serif;
  letter-spacing: 1.4px;
  pointer-events: none;
}
</style>
