<template>
    <div>
        <div class="w-75 mx-auto">
            <h3>Add Comments</h3>
            <form>
                <input type="text" placeholder="Enter your name..." class="form-control"/>
                <input type="email" placeholder="Enter your email..." class="form-control my-2"/>
                <input type="tex" placeholder="Enter your context..." class="form-control"/>
                <div class="d-flex flex-row-reverse">
                <button class="btn btn-primary mt-2">Add Commnet</button>
                </div>
            </form>
        </div>
        <div class=" w-75 mx-auto comnent" v-for="comment in comments" v-bind:key="comment.id">
            <div><b>Name: </b>{{comment.name}}</div>
            <div><b>Email: </b>{{comment.email}}</div>
            <div><b>Content: </b>{{comment.content}}</div>
    </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      comments: [
        {
          id: 1,
          name: "John",
          email: "john@gmail.com",
          content: "Lorem ipsum dolor sit amet",
        },
        {
          id: 2,
          name: "Jane", 
          email: "jane@gmail.com",
          content: "Lorem ipsum dolor sit amet",
        },
        {
          id: 3,
          name: "Bob",
          email: "bob@gmail.com",
          content: "Lorem ipsum dolor sit amet",
        },
      ],
    }
  },

  methods: {
    Increment() {
      this.Count++;
    },
    Decrement() {
      this.Count--;
    },
  },
};
</script>

<style>
.comnent {
  border: 2px solid rgb(45, 47, 148);
  padding: 10px;
  margin: 10px;
}
</style>