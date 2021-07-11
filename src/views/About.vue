<template>
  <div class="about">
    <h1>Dummy Posting Forum</h1>
    <p>This is a simple Vue application that mimics a forum where users can read and interact with posts.</p>
    <p>A user can:</p>
    <ul>
      <li>read a post and its comments.</li>
      <li>create a post by clicking on the "Create New Post" on the top right of the Home page.</li> 
      <li>delete a post by simply double-clicking on it.</li>   
    </ul>
  </div>
</template>

<style scoped>
body {
  color: #34495e;
}

.about {
  background: #eee;
  width: 90%;
  position: relative;
  left: 5%;
  height: 50vh;
  padding: 5%;
}
</style>
