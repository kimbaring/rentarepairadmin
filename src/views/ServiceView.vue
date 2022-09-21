<template>
    <SharedLayout>
    <div class="pagetitle">
      <h1>Services</h1>
      <nav>
        <ol class="breadcrumb">
          <RouterLink class="breadcrumb-item" to="/dashboard">Home</RouterLink>
          <li class="breadcrumb-item active">Service</li>

        </ol>
      </nav>
    </div><!-- End Page Title -->
    
    <div class="row">
      <div class="col-xl-8 col-md-12">
          <div class="card">
            <div class="card-body">
              <h5 class="card-title">Announcements</h5>
            
            </div>
        </div>
      </div>
      <div class="col-xl-4 col-md-12">
        <div class="card">
          <div class="card-body">
            <div class="card-title">
              Technician Service Types  
            </div>
            <ul class="list-group list-group-flush techtypes">
              <li class="list-group-item" v-for="t in task_types" :key="t">{{t}}
                <span class="closeBtn"></span>
              </li>
            </ul>
            
          </div>
        </div>
        <div class="card">
          <div class="card-body">
            <div class="card-title">
              Booking Fee 
            </div>  
          </div>
        </div>
        <div class="card">
          <div class="card-body">
            <div class="card-title">
              Testing 
            </div>  
          </div>
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
           task_types:[],
         }
       },
    mounted()
    {
        axiosReq({
          method: 'post',
          url: ciapi +'admin/config?config_field=task__problem__types',
          headers:{
              PWAuth: local.get('user_token'),
              PWAuthUser: local.get('user_id')
            }
        }).then(res=>{
          this.task_types = local.objectify(res.data.result.config_value);
        })
    }
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

.closeBtn::before,.closeBtn::after{
    position: absolute;
  content: "";
  width: 20px;
  height: 3px;
  background: #c00;
}
.closeBtn::before{
  transform: rotate(45deg);
}
.closeBtn::after{
  transform: rotate(-45deg);
}

.techtypes li{
  position: relative;
}

.techtypes li span{
  right: 20px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}



</style>