<template>
  <section class="container">
    <div class="table-responsive">
      <table class="table table-bordered table-hover capitalize">
        <thead>
          <th>no</th>
          <th>name</th>
          <th>username</th>
          <th>email</th>
          <th>phone</th>
          <th>option</th>
        </thead>
        <tbody>
          <tr v-for="(item,index) in table">
            <td>{{index+1}}</td>
            <td>{{item.name}}</td>
            <td>{{item.username}}</td>
            <td>{{item.email}}</td>
            <td>{{item.phone}}</td>
            <td>
              <button class="btn btn-info" @click="showData(item.id)">View</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="modal fade" id="view" tabindex="-1" role="dialog" aria-labelledby="exampleModalCenterTitle" aria-hidden="true">
      <div class="modal-dialog modal-dialog-centered" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLongTitle">Modal title</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <div class="table-responsive">
              <table class="table table-bordered table-hover capitalize">
                <tbody>
                  <tr>
                    <td>Name</td>
                    <td>{{preview.name}}</td>
                  </tr>
                  <tr>
                    <td>Username</td>
                    <td>{{preview.username}}</td>
                  </tr>
                  <tr>
                    <td>Email</td>
                    <td>{{preview.email}}</td>
                  </tr>
                  <tr>
                    <td>Phone</td>
                    <td>{{preview.phone}}</td>
                  </tr>
                  <tr>
                    <td>Website</td>
                    <td><a :href="preview.website">{{preview.website}}</a></td>
                  </tr>
                  <tr>
                    <td>Address</td>
                    <!-- <td>{{preview.address.street}},{{preview.address.suite}},{{preview.address.city}},{{preview.address.zipcode}}</td> -->
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import axios from 'axios'
  export default{
    data(){
      return{
        table:'',
        preview:''
      }
    },
    methods:{
      fetch(){
        axios.get('https://jsonplaceholder.typicode.com/users')
        .then((result)=>{
         this.table = result.data;
        })
      },
      showData(val){
        axios.get('https://jsonplaceholder.typicode.com/users/'+val)
        .then((result)=>{
          this.preview = result.data;
          console.log(result.data);
          setTimeout(()=>{
            $('#view').modal('show');
          },1500)
        })
      }
    },
    created(){
      this.fetch();
    }
  }
</script>
<style scoped="">
.table.capitalize th{
  text-transform: capitalize;
}
</style>