<template>
    <SharedLayout>
    <div class="pagetitle">
      <h1>Technician</h1>
      <nav>
        <ol class="breadcrumb">
          <RouterLink class="breadcrumb-item" to="/dashboard">Home</RouterLink>
          <li class="breadcrumb-item">Employee</li>
          <li class="breadcrumb-item active">Technician</li>

        </ol>
      </nav>
    </div><!-- End Page Title -->
    <div class="card">
        <div class="card-body">
            <p></p>
            <button type="button" class="btn btn-primary">Add Technician</button>
        </div>
    </div>
    <div class="card">
        <div class="card-body">
                  <h5 class="card-title">Technicians</h5> 
                  <div class="content1">
                    <ContentLoader  class="con-loader"
                      width="930"
                      height="150"
                      primaryColor="#f3f3f3"
                      secondaryColor="#cccccc">
                      <rect x="0" y="2" rx="3" ry="3" width="3000" height="35" />
                      <rect x="0" y="50" rx="3" ry="3" width="3000" height="35" />
                      <rect x="0" y="100" rx="3" ry="3" width="3000" height="35" />
                      </ContentLoader>
                  </div>
                  <div class="con-value1">
                

                    <table class="table tableborderless datatable">
                        <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Username</th>
                                <th scope="col">Firstname</th>
                                <th scope="col">Lastname</th>
                                <th scope="col">Email</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="o in objectt">
                                <th scope="row"><a href="#">{{o.id}}</a></th>
                                <td>{{o.username}}</td>
                                <td>{{o.firstname}}</td>
                                <td>{{o.lastname}}</td>
                                <td>{{o.email}}</td>
                            </tr>
                        </tbody>
                    </table>
                  </div>
                </div>
    </div>
   </SharedLayout>
</template>
<script>
import { local } from '../functions.js';
   import { axiosReq,removeFix } from '@/functions';
   import { ciapi } from '@/globals';
   import { ContentLoader } from 'vue-content-loader'

   export default{
    name: "App",
    components: {
      ContentLoader,
    },
    data() {
         return{
           objectt: [{
              Id: 0,
              username: "",
              firstname: "",
              lastname: "",
              email: "",
              status: "",
           }],
           technicians: 0,
         }
       },
       mounted(){
            axiosReq({
               method: 'post',
               url: ciapi +'users?user_role=technician&_batch=true',
               headers:{
                    PWAuth: local.get('user_token'),
                    PWAuthUser: local.get('user_id')
              }
               }).then(res=>{
                   if(res.data.success)
                   {
                      for(let data in res.data.result)
                      {
                        this.objectt.push(removeFix(res.data.result[data],'user_'));
                      }
                      this.technicians = Object.keys(res.data.result).length;
                      document.querySelector(".con-value1").style.display = "block";
                      document.querySelector(".content1").style.display = "none";
                      document.querySelector(".con-value4").style.display = "block";
                      document.querySelector(".content4").style.display = "none";
                   }
                   else
                   {
                      console.log("something went wrong");
                   }
               }).catch(err=>{
               console.log(err.response)});

               
       },
  }
</script>
<style scoped>
    @import '../../src/assets/style.css';
    @import '../../src/assets/bootstrap-icons/bootstrap-icons.css';

    .content1{
  height: 130px;
}
.con-value1{
  display: none;
}
</style>