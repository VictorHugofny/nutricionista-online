<template>
  <form>
    <Avatar/>
    <v-text-field
      v-model="name"
      :error-messages="nameErrors"
      :counter="50"
      label="Nome completo"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    >
    </v-text-field>
    <v-text-field
      v-model="email"
      :error-messages="emailErrors"
      label="E-mail"
      required
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>
    <Menuprops/>
    <v-btn
      class="submit"
      @click="submit"
    >
      Enviar
    </v-btn>

     
  </form>
</template>

<style scoped>
form{
  margin-top: 10px;
  margin-left: 150px;
  margin-right: 150px;
}

</style>

<script>
import Menuprops from '@/components/menuprops.vue'
import Avatar from '@/components/avatar.vue'
export default {
  components:{
    Menuprops,
    Avatar
  },
  methods:{
    submit: function(){
      alert("EM DESENVOLVIMENTO")
    }
  }
}
</script>