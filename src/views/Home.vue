<template>
  <div>
    <button class="btn btn-blue">Button</button>
    <input class="border border-transparent rounded-sm focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent outline-none transition-all duration-1000" type="text">
    <h1 class="bg-purple-400">Hi from Home Parent</h1>
    <div
      class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-md flex items-center space-x-4"
    >
      <div class="font-brygada">
        <div class="text-xl font-medium text-black">ChitChat</div>
        <p class="text-gray-500 ">You have a new message!</p>
      </div>
    </div>
    <div>
      <input @input="change($event)" v-model="data" type="text" class="main" :class="{'red': data && !valid}">
    </div>
    <button class="bobo outline-none  focus:outline-none border-2 border-red-400 active:bg-red-100 active:border-green-600 ">save</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: ''
    }
  },
  computed: {
    valid() {
      if(this.data.length > 4) return true
      return false
    }
  },
  methods: {
    change(e) {
      if(e.target){
        console.log(e.target);
      }
    }
  },
};
</script>

<style>
input{
  border: none;
  outline: none;
}
.main{
  border: 2px solid greenyellow;
}
.red{
  border-color: red;
}

</style>
