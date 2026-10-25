<script setup>
import { Icon } from '@iconify/vue'
import Overlay from './Overlay.vue'

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
    <div class="ticks"></div>
    <section class="box">
      <div id="center">
        <div class="hero">
        <img src="https://avatars.githubusercontent.com/u/90426410?v=4&s=110" class="base" alt="GitHub Profile Pic" />
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
      </div>
      <div id="experience">
        <icon icon="fluent-mdl2:account-management" />
        <h2>Experience</h2>
        <p>
          I'm a self-taught developer, and I started learning programming in 2022.
          I have experience with:
        </p>
        <ul>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.microsoft.com/windows/" title="Windows">
              <Icon icon="fa-brands:windows" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.kernel.org/" title="Linux">
              <Icon icon="fa-brands:linux" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.apple.com/macos/" title="macOS">
              <Icon icon="fa-brands:apple" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.android.com/" title="Android">
              <Icon icon="fa-brands:android" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://vuejs.org/" title="Vue.js">
              <Icon icon="fa-brands:vuejs" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.w3.org/html/" title="HTML5">
              <Icon icon="fa-brands:html5" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.w3.org/Style/CSS/Overview.html" title="CSS3">
              <Icon icon="fa-brands:css3" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://developer.mozilla.org/docs/Web/JavaScript" title="JavaScript">
              <Icon icon="fa-brands:js" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.electronjs.org/" title="Electron">
              <Icon icon="mdi:electron-framework" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://tauri.app/" title="Tauri">
              <Icon icon="simple-icons:tauri" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://git-scm.com" title="Git">
              <Icon icon="fa-brands:git-alt" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://github.com" title="GitHub">
              <Icon icon="fa-brands:github" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.java.com/" title="Java">
              <Icon icon="fa-brands:java" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://wikipedia.org/wiki/Shell_script" title="Shell Script">
              <Icon icon="mdi:dollar" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.arduino.cc/" title="Arduino">
              <Icon icon="simple-icons:arduino" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://isocpp.org/" title="C++">
              <Icon icon="mdi:language-cpp" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://www.python.org/" title="Python">
              <Icon icon="fa-brands:python" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://nodejs.org/" title="Node.js">
              <Icon icon="fa-brands:node" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://bun.sh/" title="Bun">
              <Icon icon="simple-icons:bun" class="button-icon" />
            </a>
          </li>
        </ul>
      </div>
    </section>
    <div class="ticks"></div>
    <section class="box">
      <div id="social">
        <icon icon="fluent-mdl2:people-add" />
        <h2>Social media</h2>
        <p>
          These are some links that you can use to contact me, or to just take a look...
        </p>
        <ul>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://github.com/lucmsilva651" title="GitHub">
              <Icon icon="fa-brands:github" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://gitlab.com/lucmsilva" title="GitLab">
              <Icon icon="fa-brands:gitlab" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://t.me/LucasAndroid" title="Telegram">
              <Icon icon="fa6-brands:telegram" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://last.fm/user/lucmsilva" title="Last.fm">
              <Icon icon="fa6-brands:lastfm-square" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://youtube.com/c/lucmsilva651" title="YouTube">
              <Icon icon="fa6-brands:youtube" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://linkedin.com/in/lucmsilva" title="LinkedIn">
              <Icon icon="fa6-brands:linkedin" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://reddit.com/u/lucmsilva" title="Reddit">
              <Icon icon="fa6-brands:reddit" class="button-icon" />
            </a>
          </li>
          <li>
            <a target="_blank" rel="noopener noreferrer" href="https://x.com/lucmsilvagg" title="X (Twitter)">
              <Icon icon="fa6-brands:twitter" class="button-icon" />
            </a>
          </li>
        </ul>
      </div>
      <div id="donate">
        <icon icon="fluent-mdl2:money" />
        <h2>Donate</h2>
        <p>If you'd like to support my work, you can donate below. Please only contribute if you can afford it, as donations are non-refundable.</p>
        <ul>
          <li><a href="/donate.txt">Donate</a></li>
        </ul>
      </div>
    </section>
    <div class="ticks"></div>
    <section id="spacer"></section>
  </overlay>
</template>
