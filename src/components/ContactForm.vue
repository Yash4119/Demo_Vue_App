<template>
    <div class="form">
        <h2>{{ title }}</h2> 
        <div class="container">
            <form @submit="postData" method="post">
          
              <label for="fname">First Name</label>
              <input type="text" id="fname" name="fname" v-model="posts.fname" placeholder="Your name..">
          
              <label for="lname">Last Name</label>
              <input type="text" id="lname" name="lname" v-model="posts.lname" placeholder="Your last name..">
          
              <label for="subject">Subject</label>
              <textarea id="msg" name="msg" v-model="posts.msg" placeholder="Write something.." style="height:100px"></textarea>
          
              <input type="submit" value="Submit">
          
            </form>
          </div>
    </div>
</template>

<script>

    export default{
        name: "ContactFrom",
        props:{
            title: String
        },
        data(){
          return{
            posts:{
              fname:'',
              lname:'',
              msg:'',
            }
          }
        },
        methods:{
          postData(e){
            console.log(this.posts)
            e.preventDefault();
          }
        }
    }
</script>

<style scoped>

input[type=text], select, textarea {
    width: 100%; /* Full width */
    padding: 12px; /* Some padding */ 
    border: 1px solid #ccc; /* Gray border */
    border-radius: 4px; /* Rounded borders */
    box-sizing: border-box; /* Make sure that padding and width stays in place */
    margin-top: 6px; /* Add a top margin */
    margin-bottom: 16px; /* Bottom margin */
    resize: vertical /* Allow the user to vertically resize the textarea (not horizontally) */
  }
  
  input[type=submit] {
    background-color: #04AA6D;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  input[type=submit]:hover {
    background-color: #45a049;
  }
  
  .container {
    margin: auto;
    width: 50%;
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 80px 80px;
  }

</style>