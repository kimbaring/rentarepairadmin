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
    <div class="card recent-sales overflow-auto">
        <div class="card-body">
          <h5 class="card-title">Technicians</h5> 
          <div id="divRequest5">
            <table id="techniciantable1" class="table tableborderless datatable" width="100%">
              <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Username</th>
                        <th scope="col">Firstname</th>
                        <th scope="col">Lastname</th>
                        <th scope="col">Email</th>
                        <th scope="col">Action</th>
                    </tr>
              </thead>
                <tfoot>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Username</th>
                        <th scope="col">Firstname</th>
                        <th scope="col">Lastname</th>
                        <th scope="col">Email</th>
                        <th scope="col">Action</th>
                    </tr>
                </tfoot>
            </table>
          </div>
        </div>
    </div>
   </SharedLayout>
</template>

<script>
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
       created(){
        $(document).ready(function () {
          if ($('#techniciantable1_wrapper').length == 1) {
            $('#divRequest5').empty().append('<table id="techniciantable1"><thead><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></thead><tfoot><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></tfoot></table>');
        }
            $('#techniciantable1').DataTable({
            ajax : {
              url : 'https://www.medicalcouriertransportation.com/rentarepair/api/users?user_role=technician&_batch=true',
              dataSrc : "result",
            },
            columns : [
              { data : "user_id" },
              { data : "user_username" },
              { data : "user_firstname"},
              { data : "user_lastname"},
              { data : "user_email"},
              { data : null, className: "center d-flex flex-nowrap", defaultContent: '<a class="btn btn-primary btn-sm" href="javascript:;">Approve</a><a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>'},
            ]
            });
        });
       }
  }
</script>
<style scoped>
    @import '../../src/assets/style.css';
    @import '../../src/assets/bootstrap-icons/bootstrap-icons.css';
</style>