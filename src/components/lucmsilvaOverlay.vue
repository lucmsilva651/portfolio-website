<template>
  <div class="overlay-wrap">
    <transition name="overlay-fade">
      <div v-if="!revealed" class="overlay" @click="onOverlayClick">
        <div class="letters">
          <span
            v-for="(l, i) in letters"
            :key="i"
            class="letter"
            :class="{ active: isActive(i) }"
            @mouseenter="setActive(i)"
          >{{ l }}</span>
        </div>

        <transition name="hint-fade" mode="out-in">
          <div v-if="currentMeaning" :key="currentMeaning" class="hint">
            {{ currentMeaning }}
          </div>
        </transition>

        <div class="instructions">click anywhere to enter</div>
      </div>
    </transition>

    <slot />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const WORD = 'lucmsilva.com'
const letters = WORD.split('')

const MEANINGS = {
  luc: 'Lucas Gabriel',
  ucm: "Marvel's UCM",
  cms: 'Content Management System (WordPress?)',
  msi: 'MSI (the brand)',
  sil: 'Still In Love (from Umamusume)',
  ilv: 'I love cats',
  lva: 'Love Vue Apps',
  'va.': 'Very awesome, period.',
  'a.c': 'Actually coding',
  '.co': 'Company of one',
  com: 'Comment section closed'
}
const revealed = ref(!window.matchMedia('(hover: hover)').matches)
const activeStart = ref(0)

function setActive(i) {
  const maxStart = letters.length - 3
  activeStart.value = Math.min(Math.max(i - 1, 0), maxStart)
}

function isActive(i) {
  return i >= activeStart.value && i < activeStart.value + 3
}

const currentMeaning = computed(() => {
  const key = WORD.slice(activeStart.value, activeStart.value + 3)
  return MEANINGS[key] || ''
})

function onOverlayClick() {
  revealed.value = true
}
</script>

<style scoped>
.overlay-wrap {
  position: relative;
  user-select: none;
}

.overlay {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1.5rem;
  background: var(--color-bg-hero);
  color: var(--color-text-primary);
  cursor: pointer;
}

.letters {
  display: flex;
  font-weight: bold;
  font-family: monospace;
  font-size: 3rem;
}

.letter {
  padding: 0 0.15rem;
  border-radius: 6px;
  transition: color 0.25s ease, transform 0.25s ease, background 0.25s ease;
  color: var(--color-text-muted);
}

.letter.active {
  color: var(--color-text-primary);
  background: var(--color-border-soft);
}

.hint {
  font-size: 1.3rem;
  letter-spacing: 0.05em;
  color: var(--color-text-secondary);
  min-height: 1.5rem;
}

.instructions {
  position: absolute;
  bottom: 2rem;
  font-size: 1.1rem;
  color: var(--color-text-muted);
}

.overlay-fade-enter-active,
.overlay-fade-leave-active {
  transition: opacity 0.4s ease;
}
.overlay-fade-enter-from,
.overlay-fade-leave-to {
  opacity: 0;
}

.hint-fade-enter-active,
.hint-fade-leave-active {
  transition: opacity 0.2s ease;
}
.hint-fade-enter-from,
.hint-fade-leave-to {
  opacity: 0;
}
</style>