<script setup>
import LightPillar from './component/LightPillar/LightPillar.vue'
</script>

<template>
  <div class="page">
    <LightPillar
      class="bg-pillars"
      top-color="#8b5cf6"
      bottom-color="#a78bfa"
      :pillar-width="1.8"
      :pillar-height="0.25"
      :pillar-rotation="-45"
    />

    <div class="stack">
      <!-- Profile picture spot -->
      <div class="avatar-ring">
        <div class="avatar-inner">
          <img src="/profilepic.webp" alt="Profile" class="avatar-img" />
        </div>
      </div>

      <!-- Title & subtitle (you can change text later) -->
      <div class="heading">
        <h1 class="title text-3xl font-semibold">TOUK3N</h1>
        <p class="subtitle text-sm text-slate-400">All of my official links below.</p>
        <p class="subtitle text-sm text-slate-400" style="margin-top: 8px;">18+ only. Gamble responsibly.</p>
      </div>

      <!-- Social row under description -->
      <div class="social-row">
        <a href="https://kick.com/Touken" target="_blank" rel="noopener noreferrer" class="social-icon social-icon--kick" aria-label="Kick">
          <img src="/kick-streaming-platform-logo-icon.svg" alt="Kick" />
        </a>
        <a href="https://x.com/Touk3n" target="_blank" rel="noopener noreferrer" class="social-icon" aria-label="Twitter / X">
          <img src="/x-social-media-black-icon.svg" alt="Twitter / X" />
        </a>
        <a href="https://www.tiktok.com/@touken.gg" target="_blank" rel="noopener noreferrer" class="social-icon" aria-label="TikTok">
          <img src="/tiktok-solo-icon.svg" alt="TikTok" />
        </a>
        <a href="https://www.instagram.com/touk3n" target="_blank" rel="noopener noreferrer" class="social-icon" aria-label="Instagram">
          <img src="/ig-instagram-icon.svg" alt="Instagram" />
        </a>
        <a href="https://discord.com/invite/4nwEFbyqJW" target="_blank" rel="noopener noreferrer" class="social-icon social-icon--discord" aria-label="Discord">
          <img src="/discord-color-icon.svg" alt="Discord" />
        </a>
      </div>

      <!-- Main link cards -->
      <div class="links">
        <a
          href="https://roobet.com/?ref=TKN"
          target="_blank"
          rel="noopener noreferrer"
          class="link-btn"
        >
          <img src="/ROOBET.png" alt="Roobet" class="link-icon" />
          <span class="link-text">Sign up on Roobet</span>
        </a>

        <a
          href="https://touken.gg/"
          target="_blank"
          rel="noopener noreferrer"
          class="link-btn"
        >
          <img src="/touken-link.png" alt="Touken" class="link-icon" />
          <span class="link-text">Explore more bonuses</span>
        </a>

        <a
          href="https://discord.com/invite/4nwEFbyqJW"
          target="_blank"
          rel="noopener noreferrer"
          class="link-btn"
        >
          <img src="/discord-color-icon.svg" alt="Discord" class="link-icon" />
          <span class="link-text">Join our community</span>
        </a>
      </div>

      <!-- Footer placeholder -->
      <div class="footer">© TKNX</div>
    </div>
  </div>
</template>

<style scoped>
.page {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 24px;
  background: radial-gradient(circle at top left, #111827, #020617 55%, #000 100%);
  color: #e5e7eb;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  position: relative;
  overflow: hidden;
}

.page::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('/toukien%20purple.png');
  background-repeat: repeat;
  background-size: 140px auto;
  opacity: 0.03;
  mix-blend-mode: screen;
  pointer-events: none;
  z-index: 0;
}

.stack {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 22px;
  position: relative;
  z-index: 2;
}

.bg-pillars {
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: 1;
}

.avatar-ring {
  width: 86px;
  height: 86px;
  border-radius: 999px;
  padding: 3px;
  background: radial-gradient(circle at 0% 0%, #a78bfa, #8b5cf6, #7c3aed);
  box-shadow: 0 18px 60px rgba(15, 23, 42, 0.95);
}

.avatar-inner {
  width: 100%;
  height: 100%;
  border-radius: inherit;
  background: #020617;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #6b7280;
  font-size: 0.75rem;
}

.avatar-img {
  width: 100%;
  height: 100%;
  border-radius: inherit;
  object-fit: cover;
}

.heading {
  text-align: center;
  max-width: 260px;
}

.title {
  font-size: 1.9rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: #ddd6fe;
}

.subtitle {
  margin-top: 6px;
  font-size: 0.9rem;
  color: #000000;
}

.social-row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 22px;
}

.social-icon {
  border: none;
  padding: 0;
  margin: 0;
  background: transparent;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.social-icon img {
  width: 25px;
  height: 25px;
  display: block;
}

.social-icon--kick img {
  width: 22.5px; /* 10% smaller than 25px */
  height: 22.5px;
}

.social-icon--discord img {
  width: 29.5px; /* 10% bigger than 25px */
  height: 29.5px;
}

.links {
  width: 100%;
  max-width: 260px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 14px;
  margin-top: 6px;
}

.link-btn {
  width: 100%;
  height: 2.75rem;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  padding: 0 1rem;
  border-radius: 10px;
  border: 1px solid rgba(139, 92, 246, 0.4);
  background: linear-gradient(135deg, rgba(23, 23, 23, 0.95) 0%, rgba(30, 25, 45, 0.9) 50%, rgba(23, 23, 23, 0.95) 100%);
  color: #e5e7eb;
  text-decoration: none;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4), inset 0 1px 0 rgba(255, 255, 255, 0.05);
  transition: all 0.25s ease;
}

.link-btn .link-icon {
  position: absolute;
  left: 1.25rem;
}

.link-btn:hover {
  border-color: rgba(167, 139, 250, 0.6);
  background: linear-gradient(135deg, rgba(30, 25, 45, 0.95) 0%, rgba(45, 35, 65, 0.9) 50%, rgba(30, 25, 45, 0.95) 100%);
  box-shadow: 0 4px 16px rgba(139, 92, 246, 0.25), inset 0 1px 0 rgba(255, 255, 255, 0.08);
  transform: translateY(-2px);
  color: #fafafa;
}

.link-icon {
  width: 24px;
  height: 24px;
  border-radius: 8px;
  background: transparent;
  object-fit: contain;
  display: block;
}

.link-text {
  font-size: 1.05rem;
  padding-left: 1.25rem;
}

.footer {
  margin-top: 10px;
  font-size: 0.75rem;
  color: #6b7280;
}

@media (max-width: 640px) {
  .page {
    padding: 16px;
  }

  .title {
    font-size: 1.5rem;
  }

  .links {
    max-width: 100%;
  }
}
</style>
