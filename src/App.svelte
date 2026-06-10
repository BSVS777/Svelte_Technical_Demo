<script>
  import TaskItem from './TaskItem.svelte';

  let newTask = $state('');
  let priority = $state('Media');
  let error = $state('');

  let tasks = $state([
    { id: 1, title: 'Preparar explicación de Svelte', priority: 'Alta', done: false },
    { id: 2, title: 'Probar demo en vivo', priority: 'Media', done: true }
  ]);

  let totalTasks = $derived(tasks.length);
  let completedTasks = $derived(tasks.filter(task => task.done).length);
  let pendingTasks = $derived(totalTasks - completedTasks);

  function addTask() {
    if (newTask.trim() === '') {
      error = 'La tarea no puede estar vacía.';
      return;
    }

    tasks = [
      ...tasks,
      {
        id: crypto.randomUUID(),
        title: newTask,
        priority,
        done: false
      }
    ];

    newTask = '';
    priority = 'Media';
    error = '';
  }

  function toggleTask(id) {
    tasks = tasks.map(task =>
      task.id === id ? { ...task, done: !task.done } : task
    );
  }

  function deleteTask(id) {
    tasks = tasks.filter(task => task.id !== id);
  }
</script>

<main>
  <h1>Svelte Lab Manager</h1>
  <p class="subtitle">Demo simple de reactividad, componentes y renderizado dinámico.</p>

  <section class="panel">
    <h2>Nueva tarea</h2>

    <input
      bind:value={newTask}
      placeholder="Ej: practicar preguntas del docente"
    />

    <select bind:value={priority}>
      <option>Alta</option>
      <option>Media</option>
      <option>Baja</option>
    </select>

    <button onclick={addTask}>Agregar</button>

    {#if error}
      <p class="error">{error}</p>
    {/if}
  </section>

  <section class="stats">
    <p>Total: <strong>{totalTasks}</strong></p>
    <p>Completadas: <strong>{completedTasks}</strong></p>
    <p>Pendientes: <strong>{pendingTasks}</strong></p>
  </section>

  <section class="panel">
    <h2>Tareas</h2>

    {#if tasks.length === 0}
      <p>No hay tareas todavía. El backlog está limpio, sospechoso pero hermoso.</p>
    {:else}
      {#each tasks as task (task.id)}
        <TaskItem
          task={task}
          onToggle={toggleTask}
          onDelete={deleteTask}
        />
      {/each}
    {/if}
  </section>
</main>