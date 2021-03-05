<template>
  <div>
    <table>
      <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Role</th>
      </tr>

      <tr v-for="(user, index) in UsersList" :key="index">
        <td>{{user.name}}</td>
        <td>{{user.age}}</td>
        <td>{{user.role}}</td>
        <td>
          <router-link :to="`/user/${index}`">User-{{index}}</router-link>
        </td>
      </tr>

      <th>

      </th>
    </table>
    <!-- <b-table striped hover>
      <b-tr>
        <b-th>Name</b-th>
        <b-th>Age</b-th>
        <b-th>Role</b-th>
      </b-tr>
      <b-tr v-for="(user, index) in UsersList" :key="index">
        <b-td>{{user.name}}</b-td>
        <b-td>{{user.age}}</b-td>
        <b-td>{{user.role}}</b-td>
        <b-td>
          <router-link :to="`/user/${index}`">User-{{index}}</router-link>
        </b-td>
      </b-tr>
    </b-table> -->
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      UsersList: [{name: 'logesh', age: 20, role: 'student'},
      {name: 'Manikandan', age: 35, role: 'faculty'},
      {name: 'Kaala', age: 21, role: 'student'},
      {name: 'Mano', age: 21, role: 'student'},
      {name: 'Karthi', age: 40, role: 'student '}]
    }
  }
}
</script>

<style scoped>
table {
  width: 75%;
  margin: 0px 150px;
}

tr:nth-child(even) 
{
  background-color: #f2f2f2;
}

tr:hover {
  background: #f2f2f2;
}

td, th {
  text-align: left;
  padding: 5px;
}

</style>
