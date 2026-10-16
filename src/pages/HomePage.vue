<script setup>
import { computed } from 'vue'
import { tasks } from '../data/tasks.js'
import TaskCard from '../components/TaskCard.vue'

const completedCount = computed(
  () => tasks.filter((task) => task.status === 'done').length,
)

const progressCount = computed(
  () => tasks.filter((task) => task.status === 'progress').length,
)

const todoCount = computed(
  () => tasks.filter((task) => task.status === 'todo').length,
)
</script>

<template>
  <f7-page name="home">
    <f7-navbar title="TaskFlow">
      <template #right>
        <f7-link href="/about/">Про нас</f7-link>
      </template>
    </f7-navbar>

    <div class="app-content">
      <header class="welcome-block">
        <h1>Мої завдання 👋</h1>
        <p>Плануй справи, виконуй цілі та відстежуй свій прогрес.</p>
      </header>

      <section class="summary-card">
        <div>
          <div class="summary-label">Усього завдань</div>
          <div class="summary-value">{{ tasks.length }}</div>
        </div>
        <div class="summary-icon">✓</div>
      </section>

      <section class="stats-grid">
        <div class="stat-card">
          <span class="stat-dot dot-green"></span>
          <span class="stat-label">Виконано</span>
          <strong>{{ completedCount }}</strong>
        </div>

        <div class="stat-card">
          <span class="stat-dot dot-blue"></span>
          <span class="stat-label">У процесі</span>
          <strong>{{ progressCount }}</strong>
        </div>

        <div class="stat-card">
          <span class="stat-dot dot-orange"></span>
          <span class="stat-label">Очікують</span>
          <strong>{{ todoCount }}</strong>
        </div>
      </section>

      <div class="section-header">
        <h2>Список завдань</h2>
        <span>{{ tasks.length }} завдань</span>
      </div>

      <div class="task-list">
        <TaskCard
          v-for="task in tasks"
          :key="task.id"
          :task="task"
        />
      </div>

      <f7-button
        class="about-button"
        fill
        large
        href="/about/"
      >
        Про застосунок
      </f7-button>
    </div>
  </f7-page>
</template>
