<template>
  <div>
    <h1>User Profiles</h1>

    <div>
      <label for="newUsername">Username:</label>
      <input type="text" id="newUsername" v-model="newUser.username" placeholder="Enter username">
      <label for="newEmail">Email:</label>
      <input type="email" id="newEmail" v-model="newUser.email" placeholder="Enter email">
      <button @click="addUser">Add User</button>
    </div>

    <ul>
      <li v-for="user in users" :key="user.id">
        <strong>{{ user.username }}</strong> - {{ user.email }}
        <button @click="removeUser(user.id)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, username: 'user1', email: 'user1@example.com' },
        { id: 2, username: 'user2', email: 'user2@example.com' },
        { id: 3, username: 'user3', email: 'user3@example.com' },
        // Add more users as needed
      ],
      newUser: {
        username: '',
        email: '',
      },
    };
  },
  methods: {
    addUser() {
      if (this.newUser.username.trim() !== '' && this.newUser.email.trim() !== '') {
        const newUser = {
          id: this.users.length + 1,
          username: this.newUser.username,
          email: this.newUser.email,
        };

        this.users.push(newUser);

        // Clear input fields
        this.newUser.username = '';
        this.newUser.email = '';
      }
    },
    removeUser(userId) {
      this.users = this.users.filter(user => user.id !== userId);
    },
  },
};
</script>

<style scoped>

</style>