
<template>
 <SharedLayout>
    <div class="pagetitle">
      <h1>Dashboard</h1>
      <nav>
        <ol class="breadcrumb">
          <RouterLink class="breadcrumb-item" to="/dashboard">Home</RouterLink>
          <li class="breadcrumb-item active">Dashboard</li>
        </ol>
      </nav>
    </div><!-- End Page Title -->

    <section class="section dashboard">
      <div class="row">

        <!-- Left side columns -->
        <div class="col-lg-8">
          <div class="row">

            <!-- Sales Card -->
            <div class="col-xxl-4 col-md-6">
              <div class="card info-card sales-card">

                <div class="filter">
                  <a class="icon" href="" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <div class="content1">
                    <ContentLoader  class="con-loader"
                      width="176"
                      height="126"
                      primaryColor="#f3f3f3"
                      secondaryColor="#cccccc">
                      <rect x="0" y="20" rx="3" ry="3" width="145" height="25" />
                      <rect x="75" y="75" rx="3" ry="3" width="30" height="35" />
                      <circle cx="30" cy="90" r="30" />
                      </ContentLoader>
                  </div>
                  <div class="con-value1">
                    <h5 class="card-title">Technicians <span></span></h5>
                  <div class="d-flex align-items-center">
                    <div class="card-icon rounded-circle d-flex align-items-center justify-content-center">
                        <i class="bi bi-people"></i>
                    </div>
                    <div class="ps-3">
                      <h6>{{technicians}}</h6>
                    </div>
                  </div>
                  </div>
                </div>

              </div>
            </div><!-- End Sales Card -->

            <!-- Revenue Card -->
            <div class="col-xxl-4 col-md-6">
              <div class="card info-card revenue-card">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <div class="content2">
                    <ContentLoader  class="con-loader"
                      width="176"
                      height="126"
                      primaryColor="#f3f3f3"
                      secondaryColor="#cccccc">
                      <rect x="0" y="20" rx="3" ry="3" width="145" height="25" />
                      <rect x="75" y="75" rx="3" ry="3" width="30" height="35" />
                      <circle cx="30" cy="90" r="30" />
                      </ContentLoader>
                  </div>
                  <div class="con-value2">
                    <h5 class="card-title">RideSharer <span></span></h5>

                  <div class="d-flex align-items-center">
                        <div class="card-icon rounded-circle d-flex align-items-center justify-content-center">
                            <i class="bi bi-people"></i>
                        </div>
                        <div class="ps-3">
                        <h6>{{ridesharer}}</h6>
                        </div>
                  </div>
                  </div>
                </div>

              </div>
            </div><!-- End Revenue Card -->

            <!-- Customers Card -->
            <div class="col-xxl-4 col-xl-12">

              <div class="card info-card customers-card">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <div class="content3">
                    <ContentLoader  class="con-loader"
                      width="176"
                      height="126"
                      primaryColor="#f3f3f3"
                      secondaryColor="#cccccc">
                      <rect x="0" y="20" rx="3" ry="3" width="145" height="25" />
                      <rect x="75" y="75" rx="3" ry="3" width="30" height="35" />
                      <circle cx="30" cy="90" r="30" />
                      </ContentLoader>
                  </div>
                  <div class="con-value3">
                    <h5 class="card-title">Towing <span></span></h5>

                  <div class="d-flex align-items-center">
                    <div class="card-icon rounded-circle d-flex align-items-center justify-content-center">
                      <i class="bi bi-people"></i>
                    </div>
                    <div class="ps-3">
                      <h6>{{towtruck}}</h6>
                    </div>
                  </div>
                  </div>

                </div>
              </div>

            </div><!-- End Customers Card -->

            <!-- Reports -->
            <div class="col-12">
              <div class="card">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <h5 class="card-title">Reports <span>/Today</span></h5>

                  <!-- Line Chart -->
                  <div id="reportsChart"></div>
                  <!-- End Line Chart -->

                </div>

              </div>
            </div><!-- End Reports -->

            <!-- Recent Sales -->
            <div class="col-12">
              <div class="card recent-sales overflow-auto">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <h5 class="card-title">Technicians</h5>
                  <div id="divRequest1">
                    <table id="techniciantable" class="display" width="100%">
                        <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Username</th>
                                <th scope="col">Firstname</th>
                                <th scope="col">Lastname</th>
                                <th scope="col">Email</th>
                                <th scope="col">Status</th>
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
                                <th scope="col">Status</th>
                                <th scope="col">Action</th>
                            </tr>
                        </tfoot>
                    </table>
                  </div>
                </div>

            </div>
            </div><!-- End Recent Sales -->
            <!-- Recent Sales -->
            <div class="col-12">
              <div class="card recent-sales overflow-auto">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>

                <div class="card-body">
                  <h5 class="card-title">Ride Sharer <span></span></h5> 
                  <div id="divRequest2">
                    <table id="ridesharerTable" class="table tableborderless datatable"  width="100%">
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
            </div><!-- End Recent Sales -->
            <div class="col-12">
              <div class="card recent-sales overflow-auto">

                <div class="filter">
                  <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
                  <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                    <li class="dropdown-header text-start">
                      <h6>Filter</h6>
                    </li>

                    <li><a class="dropdown-item" href="#">Today</a></li>
                    <li><a class="dropdown-item" href="#">This Month</a></li>
                    <li><a class="dropdown-item" href="#">This Year</a></li>
                  </ul>
                </div>
                  <div class="card-body">
                  <h5 class="card-title">Towing Members</h5>               
                  <div id="divRequest3">
                    <table id="TowingTable" class="table tableborderless datatable" width="100%">
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
            </div>
            

          </div>
        </div><!-- End Left side columns -->

        <!-- Right side columns -->
        <div class="col-lg-4">

          

          <!-- Budget Report -->
          <div class="card">
            <div class="filter">
              <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
              <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                <li class="dropdown-header text-start">
                  <h6>Filter</h6>
                </li>

                <li><a class="dropdown-item" href="#">Today</a></li>
                <li><a class="dropdown-item" href="#">This Month</a></li>
                <li><a class="dropdown-item" href="#">This Year</a></li>
              </ul>
            </div>

            <div class="card-body pb-0">
              <h5 class="card-title">Budget Report <span>| This Month</span></h5>

              <div id="budgetChart" style="min-height: 400px;" class="echart"></div>


            </div>
          </div><!-- End Budget Report -->

          
          <!-- <div class="card">
            <div class="filter">
              <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
              <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                <li class="dropdown-header text-start">
                  <h6>Filter</h6>
                </li>

                <li><a class="dropdown-item" href="#">Today</a></li>
                <li><a class="dropdown-item" href="#">This Month</a></li>
                <li><a class="dropdown-item" href="#">This Year</a></li>
              </ul>
            </div>

            <div class="card-body pb-0">
              <h5 class="card-title">Website Traffic <span>| Today</span></h5>

              <div id="trafficChart" style="min-height: 400px;" class="echart"></div>

            </div>
          </div> -->

          <!-- News & Updates Traffic -->
          <div class="card">
            <div class="filter">
              <a class="icon" href="#" data-bs-toggle="dropdown"><i class="bi bi-three-dots"></i></a>
              <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
                <li class="dropdown-header text-start">
                  <h6>Filter</h6>
                </li>

                <li><a class="dropdown-item" href="#">Today</a></li>
                <li><a class="dropdown-item" href="#">This Month</a></li>
                <li><a class="dropdown-item" href="#">This Year</a></li>
              </ul>
            </div>

            <div class="card-body pb-0">
              <h5 class="card-title">News &amp; Updates <span>| Today</span></h5>

              <div class="news">
                <div class="post-item clearfix">
                  <h4><a href="#">Nihil blanditiis at in nihil autem</a></h4>
                  <p>Sit recusandae non aspernatur laboriosam. Quia enim eligendi sed ut harum...</p>
                </div>

                <div class="post-item clearfix">
                  <h4><a href="#">Quidem autem et impedit</a></h4>
                  <p>Illo nemo neque maiores vitae officiis cum eum turos elan dries werona nande...</p>
                </div>

                <div class="post-item clearfix">
                  <h4><a href="#">Id quia et et ut maxime similique occaecati ut</a></h4>
                  <p>Fugiat voluptas vero eaque accusantium eos. Consequuntur sed ipsam et totam...</p>
                </div>

                <div class="post-item clearfix">
                  <h4><a href="#">Laborum corporis quo dara net para</a></h4>
                  <p>Qui enim quia optio. Eligendi aut asperiores enim repellendusvel rerum cuder...</p>
                </div>

                <div class="post-item clearfix">
                  <h4><a href="#">Et dolores corrupti quae illo quod dolor</a></h4>
                  <p>Odit ut eveniet modi reiciendis. Atque cupiditate libero beatae dignissimos eius...</p>
                </div>

              </div><!-- End sidebar recent posts-->

            </div>
          </div><!-- End News & Updates -->

        </div><!-- End Right side columns -->

      </div>
    </section>

 </SharedLayout>
</template>
<script>

  import { local } from '../functions.js';
   import { axiosReq,removeFix,elementLoad } from '@/functions';
   import { ciapi } from '@/globals';
   import { ContentLoader } from 'vue-content-loader';

  const value = ({
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
           objectr: [{
              Id: 0,
              username: "",
              firstname: "",
              lastname: "",
              email: "",
              status: "",
           }],
           objecttw: [{
              Id: 0,
              username: "",
              firstname: "",
              lastname: "",
              email: "",
              status: "",
           }],
           technicians: 0,
           ridesharer: 0,
           towtruck: 0,
         }
       },
       mounted(){
        $(document).ready(function () {
          if ($('#techniciantable_wrapper').length == 1) {
            $('#divRequest1').empty().append('<table id="techniciantable"><thead><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></thead><tfoot><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></tfoot></table>');
        }
          $('#techniciantable').dataTable({
                ajax : {
                  url: 'https://www.medicalcouriertransportation.com/rentarepair/api/users?user_role=technician&_batch=true',
                  dataSrc: 'result'
                },
                columns : [
                  { data : "user_id" },
                  { data : "user_username" },
                  { data : "user_firstname"},
                  { data : "user_lastname"},
                  { data : "user_email"},
                  { data : "user_isdeactivated",
                    render: function(data){
                      var statusword = "";
                      var statusclass = "";
                      switch(data){
                        case '1':
                            statusword = 'Block';
                            statusclass = 'important';
                            break;
                        case '4':
                            statusword = 'Pending';
                            statusclass = 'warning';
                            break;
                        case '0':
                            statusword = 'Approved';
                            statusclass = 'success';
                            break;
                        case '2':
                            statusword = 'Not Verified';
                            statusclass = 'Danger';
                            break;
                        case '3':
                            statusword = 'Denied';
                            statusclass = 'primary';
                            break;
                        default:
                          break;
                      }
                      return '<span class="p-1 mb-1 bg-' + statusclass + ' text-white">' + statusword + '</span>'
                    }
                  },
                  { data : null,
                    render: function(data, type, row, meta){
                      var statusword;
                      switch(row.user_isdeactivated){
                        case '1':
                            statusword = 'Block';
                            break;
                        case '4':
                            statusword = 'Pending';
                            break;
                        case '0':
                            statusword = 'Approved';
                            break;
                        case '2':
                            statusword = 'NotVerified';
                            break;
                        case '3':
                            statusword = 'Denied';
                            break;
                        default:
                          break;
                      }
                      if(statusword == "Denied" || statusword == "Approved")
                      {
                        return '<a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>'
                      }
                      else if(statusword == "Block")
                      {
                        return '<a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Unblock</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>'
                      }
                      else if( statusword == "Pending" || statusword == "NotVerified")
                      {
                        return '<a data-value='+data+' class="btn btn-primary btn-sm logMe" href=javascript":;">Approve</a><a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a><a class="btn btn-warning btn-sm" href="javascript:;">Deny</a>'
                      }
                    }
                  },
                ],
            });
            elementLoad('.logMe').then(()=>{
              document.querySelectorAll('.logMe').forEach(el=>{
                el.onclick = e=>{
                  console.log("clicked");
                  value.methods.approveEmp(e.target.dataset.value);
                }
              })
            });




            if ($('#ridesharerTable_wrapper').length == 1) {
            $('#divRequest2').empty().append('<table id="ridesharerTable"><thead><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></thead><tfoot><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></tfoot></table>');
        }
          $('#ridesharerTable').dataTable({
                ajax : {
                  url: 'https://www.medicalcouriertransportation.com/rentarepair/api/users?user_role=ride_sharer&_batch=true',
                  dataSrc: 'result'
                },
                columns : [
                  { data : "user_id" },
                  { data : "user_username" },
                  { data : "user_firstname"},
                  { data : "user_lastname"},
                  { data : "user_email"},
                  { data : null, className: "center d-flex flex-nowrap", defaultContent: '<a class="btn btn-primary btn-sm" href="javascript:;">Approve</a><a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>'},
                ],
            });
            if ($('#TowingTable_wrapper').length == 1) {
            $('#divRequest3').empty().append('<table id="TowingTable"><thead><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></thead><tfoot><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></tfoot></table>');
        }
          $('#TowingTable').dataTable({
                ajax : {
                  url: 'https://www.medicalcouriertransportation.com/rentarepair/api/users?user_role=tow_truck_operator&_batch=true',
                  dataSrc: 'result'
                },
                columns : [
                  { data : "user_id" },
                  { data : "user_username" },
                  { data : "user_firstname"},
                  { data : "user_lastname"},
                  { data : "user_email"},
                  {
                    data : "user_id",
                    render : function(data){
                      return `<a class="btn btn-primary btn-sm" href="javascript:;">Approve</a><a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>`
                    }
                  }
                ],
            });
        });
            axiosReq({
               method: 'post',
               url: ciapi +'users?user_role=technician&_batch=true',
               data: "",
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
                   }
                   else
                   {
                      console.log("something went wrong");
                   }
               }).catch(err=>{
               console.log(err.response)});

               axiosReq({
               method: 'post',
               url: ciapi +'users?user_role=ride_sharer&_batch=true',
               headers:{
                    PWAuth: local.get('user_token'),
                    PWAuthUser: local.get('user_id')
              }
               }).catch(err=>{
               console.log(err.response);
               }).then(res=>{
                   console.log(res.data);
                   if(res.data.success)
                   {
                      for(let data in res.data.result)
                      {
                        this.objectr.push(removeFix(res.data.result[data],'user_'));
                      }
                      this.ridesharer = Object.keys(res.data.result).length;
                      document.querySelector(".con-value2").style.display = "block";
                      document.querySelector(".content2").style.display = "none";
                   }
                   else
                   {
                      console.log("something went wrong");
                   }
               });
               axiosReq({
               method: 'post',
               url: ciapi +'users?user_role=tow_truck_operator&_batch=true',
               headers:{
                    PWAuth: local.get('user_token'),
                    PWAuthUser: local.get('user_id')
              }
               }).catch(err=>{
               console.log(err.response);
               }).then(res=>{
                   if(res.data.success)
                   {  
                      this.towtruck = Object.keys(res.data.result).length;
                      document.querySelector(".con-value3").style.display = "block";
                      document.querySelector(".content3").style.display = "none";
                      for(let data in res.data.result)
                      {
                        this.objecttw.push(removeFix(res.data.result[data],'user_'));
                      }
                   }
                   else
                   {
                      console.log("something went wrong");
                   }
               });
               
       },
       methods : {
        approveEmp(data){
          axiosReq({
                method: 'post',
                url: ciapi+'users/update?user_id='+data,
                headers:{
                    PWAuth: local.get('user_token'),
                    PWAuthUser: local.get('user_id')
                },
                data:{isdeactivated:0}
            }).catch(()=>{
                console.log(res);
            }).then(res=>{
              console.log("success");
              if ($('#techniciantable_wrapper').length == 1) {
                  $('#divRequest1').empty().append('<table id="techniciantable"><thead><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></thead><tfoot><tr><th scope="col">#</th><th scope="col">Username</th><th scope="col">Firstname</th><th scope="col">Lastname</th><th scope="col">Email</th><th scope="col">Action</th></tr></tfoot></table>');
              }
                $('#techniciantable').dataTable({
                      ajax : {
                        url: 'https://www.medicalcouriertransportation.com/rentarepair/api/users?user_role=technician&_batch=true',
                        dataSrc: 'result'
                      },
                      columns : [
                        { data : "user_id" },
                        { data : "user_username" },
                        { data : "user_firstname"},
                        { data : "user_lastname"},
                        { data : "user_email"},
                        { data : "user_id",
                          render: function(data){
                            return '<a data-value='+data+' class="btn btn-primary btn-sm logMe" href="javascript:;">Approve</a><a class="btn btn-danger btn-sm me-1 ms-1" href="javascript:;">Block</a><a class="btn btn-warning btn-sm" href="javascript:;">Edit</a>'
                          }
                        },
                      ],
                  });
            });
        }
       }
  })
  export default value
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
.content2{
  height: 130px;
}
.con-value2{
  display: none;
}
.content3{
  height: 130px;
}
.con-value3{
  display: none;
}
.content4{
  height: 130px;
}
.con-value4{
  display: none;
}
.content5{
  height: 130px;
}
.con-value5{
  display: none;
}
.content6{
  height: 130px;
}
.con-value6{
  display: none;
}
</style>