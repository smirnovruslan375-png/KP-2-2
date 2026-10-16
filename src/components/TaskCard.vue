<script setup>
defineProps({
  task: {
    type: Object,
    required: true,
  },
})

const statusLabels = {
  todo: 'Очікує',
  progress: 'У процесі',
  done: 'Виконано',
}

const priorityLabels = {
  low: 'Низький пріоритет',
  medium: 'Середній пріоритет',
  high: 'Високий пріоритет',
}

const statusClasses = {
  todo: 'status-todo',
  progress: 'status-progress',
  done: 'status-done',
}

const priorityClasses = {
  low: 'priority-low',
  medium: 'priority-medium',
  high: 'priority-high',
}
</script>

<template>
  <article class="task-card">
    <div class="task-card__top">
      <span
        class="task-card__status"
        :class="statusClasses[task.status] || 'status-todo'"
      >
        {{ statusLabels[task.status] || 'Очікує' }}
      </span>

      <span
        class="task-card__priority"
        :class="priorityClasses[task.priority] || 'priority-low'"
      >
        {{ priorityLabels[task.priority] || 'Низький пріоритет' }}
      </span>
    </div>

    <h3 class="task-card__title">
      {{ task.title }}
    </h3>

    <p class="task-card__description">
      {{ task.category }}
    </p>
  </article>
</template>
