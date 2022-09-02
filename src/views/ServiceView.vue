<template>
    <SharedLayout>
    <div class="pagetitle">
      <h1>Services</h1>
      <nav>
        <ol class="breadcrumb">
          <RouterLink class="breadcrumb-item" to="/dashboard">Home</RouterLink>
          <li class="breadcrumb-item active">Services</li>

        </ol>
      </nav>
    </div><!-- End Page Title -->
    <div class="card">
        <div class="card-body">
            <p></p>
            <button type="button" class="btn btn-primary">Add Services</button>
        </div>
    </div>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">Services Table</h5>

            <!-- Default Table -->
            <table class="table">
            <thead>
                <tr>
                <th scope="col">#</th>
                <th scope="col">Name</th>
                <th scope="col">Position</th>
                <th scope="col">Age</th>
                <th scope="col">Start Date</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                <th scope="row">1</th>
                <td>Brandon Jacob</td>
                <td>Designer</td>
                <td>28</td>
                <td>2016-05-25</td>
                </tr>
                <tr>
                <th scope="row">2</th>
                <td>Bridie Kessler</td>
                <td>Developer</td>
                <td>35</td>
                <td>2014-12-05</td>
                </tr>
                <tr>
                <th scope="row">3</th>
                <td>Ashleigh Langosh</td>
                <td>Finance</td>
                <td>45</td>
                <td>2011-08-12</td>
                </tr>
                <tr>
                <th scope="row">4</th>
                <td>Angus Grady</td>
                <td>HR</td>
                <td>34</td>
                <td>2012-06-11</td>
                </tr>
                <tr>
                <th scope="row">5</th>
                <td>Raheem Lehner</td>
                <td>Dynamic Division Officer</td>
                <td>47</td>
                <td>2011-04-19</td>
                </tr>
            </tbody>
            </table>
            <!-- End Default Table Example -->
        </div>
    </div>
   </SharedLayout>
</template>
<script>

</script>
<style scoped>
    @import '../../src/assets/style.css';
    @import '../../src/assets/bootstrap-icons/bootstrap-icons.css';
</style>