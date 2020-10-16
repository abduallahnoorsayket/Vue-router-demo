<template>
  <div id="app" class="demo">
    <h1  id="info">Simple Form</h1>

    <form action="/dataCollectionLocation" method="post" autocomplete='on'>
      <div v-for="item in formItems" :key="item.id" class='form-item'>
            <div v-if="item.id === 'password' && item.type==='password'  &&  item.label==='Password'">
             <label :for="item.id">{{ item.label }}: </label>
            <input :type="item.type" :id="item.id" :name="item.id" v-model="item.value" aria-labelledby="info item" aria-describedby="nameDescription">
            <p id="nameDescription">Please provide  passssword 8 charecters long.</p>
            </div>
            <div v-else>
            <label :for="item.id">{{ item.label }}: </label>
            <input :type="item.type" :id="item.id" :name="item.id" v-model="item.value" aria-labelledby="info item" aria-describedby="nameDescription">
            </div>
        

        <!-- <h1 v-if="awesome">Vue is awesome!</h1> -->

      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formItems: [
        {
          label: 'First Name',
          id: 'first-name',
          type: 'text',
          value: ''
        },
        {
          label: 'Last Name',
          id: 'last-name',
          type: 'text',
          value: ''
        },
        {
          label: 'Email',
          id: 'email',
          type: 'email',
          value: ''
        },
        {
          label: 'Password',
          id: 'password',
          type: 'password',
          value: ''
        },
      ]
    };
  }
};
</script>

<style>
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}

.form-item {
  margin: 1em auto;
}

.form-item label {
  /* display: block; */
}

button {
  font-size: 1em;
}

</style>