<script>
  let { task, onToggle, onDelete } = $props();
</script>

<article class:done={task.done} class="task">
  <div>
    <h3>{task.title}</h3>
    <p>Prioridad: {task.priority}</p>
  </div>

  <div class="actions">
    <button onclick={() => onToggle(task.id)}>
      {task.done ? 'Reabrir' : 'Completar'}
    </button>

    <button onclick={() => onDelete(task.id)}>
      Eliminar
    </button>
  </div>
</article>