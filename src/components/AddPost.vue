<template>
  <div class="add-post">
    <div class="row mb-3">
      <div class="col text-right">
        <button class="btn btn-primary" v-on:click="formShow">Create New Post</button>
      </div>
    </div>
    <div class="card bg-bright mb-3" v-if="formDiv">
      <div class="card-body">
          <form @submit.prevent="addPost">
            <div class="form-group">
              <label class="mb-3">Post Title</label>
              <input v-model="title" type="text" name="title" class="form-control mb-3" placeholder="Enter post title">
            </div>
            <div class="form-group">
              <label class="mb-3">Post Details</label>
              <textarea v-model="body" name="body" class="form-control mb-3" placeholder="Enter post details here..."></textarea>
            </div>
            <div class="row">
              <div class="col-10">
                <button class="btn btn-block btn-success">Create Post</button>
              </div>
            </div>
          </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AddPost",
  data() {
    return {
      formDiv: false,
      title: "",
      body: ""
    };
  },
  methods: {
    formShow() {
      this.formDiv = true;
    },
    addPost() {
      const newPost = {
        title: this.title,
        body: this.body
      };
      this.$emit("add-post", newPost);
      (this.title = ""), (this.body = "");
    }
  }
};
</script>

<style>
  .text-right {
    text-align: right;
  }
</style>