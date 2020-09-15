<template>
  <div class="users-table">
    <div class="table-name">
      <h1> Users Table </h1>
    </div>
    <!-- Table -->
    <table>
      <!-- Header -->
      <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Department</th>
        <th>age</th>
        <th>Start Date</th>
        <th>Salary</th>
        <th>Email</th>
      </tr>

      <!-- Rows -->
      <!-- We itterate to render one row per database item -->
      <tr v-for="user in users" :key="user.id">
        <td>
          {{ user.id }}
        </td>
        <td>
          {{ user.name }}
        </td>
        <td>
          {{ user.department }}
        </td>
        <td>
          {{ user.age }}
        </td>
        <td>
          {{ user.startDate }}
        </td>
        <td>
          {{ user.salary }}
        </td>
        <td>
          {{ user.email }}
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Users Table',
  props: ['users'],
}
</script>

<style scoped>
.users-table {
  border: 1px solid #E4E4E4;
  margin: 2em;
}
.table-name {
  background-color: #F7F7F7;
  border: 1px solid #E4E4E4;
}
h1 {
  text-align: left;
  font-size: 1.1em;
  padding: 1em 0.5em;
}
table {
  width: calc(100% - 2em);
  border-collapse: collapse;
  margin: 1em;
}
th, td {
  padding: 1em 2em;
  border: 1px solid  #E4E4E4;
}
th {
  font-weight: 500;
}
</style>