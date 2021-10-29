<template>
  <div>
    <h3>Ibk's TODO List</h3>

    <form id="todo-form">
      <input id="update" placeholder="New Task" type="text" value="" />
      <button type="submit" v-on:click.prevent="addTodo">Add Item</button>
    </form>

    <ol>
      <li v-for="(item, i) in list" v-bind:key="item.id">
        {{ i + 1 }}. {{ item }}
        <button class="remove" v-on:click="removeTask">Delete</button>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [],
    };
  },
  methods: {
    addTodo: function () {
      let input = document.getElementById("update");
      this.list = this.list.concat(input.value);
      input.value = "";
    },
    removeTask(index) {
      this.list.splice(index, 1);
    },
  },
};
</script>

<style scope>
div {
  box-sizing: border-box;
  width: 550px;
  margin: 50px auto 0 auto;
  text-align: center;
  border-radius: 5px;
  box-shadow: 0 0 5px #252525;
}
form {
  display: flex;
  justify-content: space-evenly;
}
span {
  cursor: pointer;
}

h3 {
  background-color: #252525;
  padding: 10px 90px;
  margin: 0;
  color: #fff;
}

ol {
  padding-left: 0;
}

li {
  padding: 20px 0 20px 30px;
  margin: 1px 0 1px 0;
  border-bottom: 1px solid black;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 20px;
  color: white;
  font-weight: 500;
}
input,
button {
  padding: 12px;
  background: #fe803e;
  border: none;
  border-radius: 2px;
  cursor: pointer;
  font-size: 20px;
  color: #fff;
  box-shadow: 0 5px 7px rgba(0, 0, 0, 0.15);
}
input:focus {
  outline: none;
}

input {
  width: 75%;
  background: white;
  color: black;
}

button {
  width: 25%;
  border: 1px solid rgb(214, 193, 193);
  outline: none;
}

button:hover {
  background: #d4b178;
}

.remove {
  margin-right: 30px;
}

.remove:hover {
  background: red;
}
</style>