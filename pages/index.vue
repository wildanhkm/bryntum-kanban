<template>
  <div>
    <BryntumProjectModel ref="project" v-bind="projectConfig" :tasks="tasks" />
    <BryntumTaskBoard ref="taskboard" v-bind="taskBoardConfig" />
  </div>
</template>

<script>
import { BryntumProjectModel, BryntumTaskBoard } from '@bryntum/taskboard-vue-3'
export default {
  name: 'IndexPage',

  components: {
    BryntumProjectModel,
    BryntumTaskBoard,
  },

  data() {
    return {
      taskBoardConfig: {
        columns: ['todo', 'doing', 'done'],
        columnField: 'status',
      },
      projectConfig: {},
      tasks: [
        { id: 1, name: 'My first task', status: 'doing' },
        { id: 2, name: 'My second task', status: 'todo' },
      ],
    }
  },
}
</script>
