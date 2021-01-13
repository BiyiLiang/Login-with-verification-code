 <template>
    <loginTextfield></loginTextfield>
    <div class="router">
        <router-link style="background-color:#F98C93; padding:10px;" to="/">Home</router-link> 
        <router-link style="background-color:#F98C93; padding:10px;" to="/about">About</router-link>
    </div>
</template>

<script>
import loginTextfield from '@/components/loginTextfield.vue';

export default {
    name: 'login',
    components: {
      loginTextfield
      },
    data: function() {
      return {
        state: 1
      }
    },
    computed: {
      
    }
    }
</script>

<style scoped>

.router{
  background-color:#F98C93;
  padding:20px;
  color: white;
}
</style>

    