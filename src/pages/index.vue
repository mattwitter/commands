<template>
  <v-sheet 
  :elevation="24"
  width="80%"
  height="100%"
  class="pa-4 text-center mx-auto"
  >
    <v-table>
      <thead>
        <tr>
          <th class="text-center ml-8" style="align-content: center; font-size: 32px">
            Channel Commands
          </th>
          <th></th>
        </tr>
        <tr>
          <th class="text-center">
            Command
          </th>
          <th class="text-center">
            Response
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in commands"
          :key="item.name"
        >
          <td>{{ item.command }}</td>
          <td>{{ item.response }}</td>
        </tr>
      </tbody>
    </v-table>
  </v-sheet>
</template>
<script>
  export default {
    data () {
      return {
        commands: [
          {
            command: '!today',
            response: 'Display today\'s logged drops' 
          },
          {
            command: '!today add item',
            response: 'Add an item to today\'s item log'
          },
          {
            command: '!today clear',
            response: 'Clear today\'s logged drops'
          }
        ],
      }
    },
  }
</script>