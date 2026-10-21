<script setup>
import Overlay from './Overlay.vue'
import { Icon } from '@iconify/vue'

const k = () => window.location.href = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";

const calcAge = (d) => {
  const x = new Date();
  const y = new Date(d);
  let z = x.getFullYear() - y.getFullYear();
  const monthDiff = x.getMonth() - y.getMonth();
  const dayDiff = x.getDate() - y.getDate();
  if (monthDiff < 0 || (monthDiff === 0 && dayDiff < 0)) {
    z--;
  }
  return z;
}
</script>

<template>
  <overlay>
    <section id="center">
      <div class="hero">
        <img src="https://avatars.githubusercontent.com/u/90426410?v=4" class="base" width="170" height="179" alt="" />
      </div>
      <div>
        <h1>Welcome!</h1>
        <p>
          I'm Lucas, a {{ calcAge("2009/07/07") }} y.o. student from Brazil. I
          have knowledge with web development, hardware, etc.
        </p>
      </div>
      <button type="button" class="counter" @click="k">
        Click here
      </button>
    </section>
    <div class="ticks"></div>
    <section id="next-steps">
      <div id="social">
        <icon icon="fluent-mdl2:people-add" />
        <h2>Social media</h2>
        <p>
          These are some links that you can use to contact me, or to just take a look...
        </p>
        <ul>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://github.com/lucmsilva651">
              <icon icon="fa-brands:github" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://gitlab.com/lucmsilva">
              <Icon icon="fa-brands:gitlab" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://t.me/LucasAndroid">
              <Icon icon="fa6-brands:telegram" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://last.fm/user/lucmsilva">
              <Icon icon="fa6-brands:lastfm-square" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://youtube.com/c/lucmsilva651">
              <Icon icon="fa6-brands:youtube" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://linkedin.com/in/lucmsilva">
              <Icon icon="fa6-brands:linkedin" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://reddit.com/u/lucmsilva">
              <Icon icon="fa6-brands:reddit" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://x.com/lucmsilvagg">
              <Icon icon="fa6-brands:twitter" class="button-icon" />
            </a>
          </li>
        </ul>
      </div>
      <div id="exp">
        <icon icon="fluent-mdl2:account-management" />
        <h2>Experience</h2>
        <p>
          I'm a self-taught developer, and I started learning programming in 2022.
          I have experience with:
        </p>
        <ul>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.microsoft.com/windows/">
              <Icon icon="fa-brands:windows" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.kernel.org/">
              <Icon icon="fa-brands:linux" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.apple.com/macos/">
              <Icon icon="fa-brands:apple" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.android.com/">
              <Icon icon="fa-brands:android" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://vuejs.org/">
              <Icon icon="fa-brands:vuejs" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.w3.org/html/">
              <Icon icon="fa-brands:html5" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.w3.org/Style/CSS/Overview.html">
              <Icon icon="fa-brands:css3" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://developer.mozilla.org/docs/Web/JavaScript">
              <Icon icon="fa-brands:js" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.electronjs.org/">
              <Icon icon="mdi:electron-framework" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://tauri.app/">
              <Icon icon="simple-icons:tauri" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://git-scm.com">
              <Icon icon="fa-brands:git-alt" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://github.com">
              <Icon icon="fa-brands:github" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.java.com/">
              <Icon icon="fa-brands:java" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://wikipedia.org/wiki/Shell_script">
              <Icon icon="mdi:dollar" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.arduino.cc/">
              <Icon icon="simple-icons:arduino" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://isocpp.org/">
              <Icon icon="mdi:language-cpp" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.python.org/">
              <Icon icon="fa-brands:python" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://nodejs.org/">
              <Icon icon="fa-brands:node" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://bun.sh/">
              <Icon icon="simple-icons:bun" class="button-icon" />
            </a>
          </li>
        </ul>
      </div>
    </section>
    <div class="ticks"></div>
    <section id="spacer"></section>
    <section id="donate">
      <icon icon="fluent-mdl2:money" />
      <h2>Donate</h2>
      <p>Only donate if you actually don't need the money, I will not do refunds.</p>
      <ul>
        <li>Pix (Brazil / BRL): lucmsilva651@gmail.com</li>
        <li>Cryptocurrency: <a href="/crypto.txt">Click here to see options</a></li>
      </ul>
    </section>
  </overlay>
</template>
