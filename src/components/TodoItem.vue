<template>
  <div class="todo-card">
    <div>
      <div>
        {{ todo.title }}
      </div>
      <div>
        {{ todo.project }}
      </div>
      <div>
        <span>
          <i class='edit icon'></i>
        </span>
      </div>
    </div>
    <div v-show="todo.done">
      Completed
    </div>
    <div v-show="!todo.done">
      Complete
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  props: ['todo'],
};
</script>
