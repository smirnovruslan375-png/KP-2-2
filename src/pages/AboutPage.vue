<template>
  <f7-page name="about">
    <f7-navbar title="Про TaskFlow" back-link="Назад" />

    <div class="app-content">
      <header class="welcome-block">
        <h1>Про застосунок</h1>
        <p>
          Усе необхідне для організації справ і контролю
          особистої продуктивності в одному місці.
        </p>
      </header>

      <section class="about-hero">
        <div class="about-logo">✓</div>
        <h2>TaskFlow</h2>
        <p class="about-version">Менеджер особистих завдань</p>
        <p>
          TaskFlow — прогресивний вебзастосунок для організації
          завдань і відстеження особистої продуктивності.
        </p>
      </section>

      <div class="section-header">
        <h2>Використані технології</h2>
      </div>

      <section class="technology-list">
        <article class="technology-card">
          <div class="technology-icon icon-vue">V</div>
          <div class="technology-info">
            <h3>Vue 3</h3>
            <p>Створення інтерфейсу користувача</p>
          </div>
        </article>

        <article class="technology-card">
          <div class="technology-icon icon-framework">F7</div>
          <div class="technology-info">
            <h3>Framework7</h3>
            <p>Готові компоненти інтерфейсу</p>
          </div>
        </article>

        <article class="technology-card">
          <div class="technology-icon icon-vite">V</div>
          <div class="technology-info">
            <h3>Vite</h3>
            <p>Розробка та збірка проєкту</p>
          </div>
        </article>

        <article class="technology-card">
          <div class="technology-icon icon-pwa">P</div>
          <div class="technology-info">
            <h3>PWA</h3>
            <p>Кешування та можливість встановлення</p>
          </div>
        </article>
      </section>

      <f7-button
        class="about-button"
        fill
        large
        href="/"
      >
        На головну
      </f7-button>
    </div>
  </f7-page>
</template>
