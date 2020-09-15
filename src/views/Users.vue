<template>
  <div class="user">  
    <PanelHeader :name="'Admin Users'" />
    <UsersTable :users="users" />    
  </div>
</template>

<script>
import PanelHeader from '@/components/PanelHeader.vue'
import UsersTable from '@/components/UsersTable.vue'
import users from '@/store/database'
export default {
  name: 'Users',
  components: { PanelHeader, UsersTable },
  data() {
    return {
      users
    }
  },
  mounted() {
    this.users = users
  }
}
</script>
