<template>
  <div class="page-holder bg-gray-100">
     <header class="header bg-white shadow align-self-end py-3 px-xl-5 w-100">
          <div class="container-fluid">
            <div class="row">
              <div class="col-md-6 text-center text-md-start fw-bold">
                <p class="mb-2 mb-md-0 fw-bold">Torre-Test</p>
              </div>
              <div class="col-md-6 text-center text-md-end text-gray-400">
                <p class="mb-0" :names='names'>{{ names }}</p>
              </div>
            </div>
          </div>
        </header>
        <div class="container-fluid px-lg-4 px-xl-5 contentDiv">
              <!-- Page Header-->
              <div class="page-header mb-4">
                <h3 class="page-heading">Profile</h3>
              </div>
          <section>
            <div class="row">
              <div class="col-lg-4">
                <div class="card card-profile mb-4">
                  <div class="card-header" style="background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROdNIejFmjeKC5u6Xq2yqOCa5y-uJseTCTfA&usqp=CAU);"> </div>
                  <div class="card-body text-center">
                    <img class="card-profile-img" :src=picture alt="applicant picture">
                    <h3 class="mb-3" :names='names'>{{ names }}</h3>
                    <p class="mb-4" :title='title'>{{title}}</p>
                    <button class="btn btn-outline-dark btn-sm"><span class="fab fa-twitter"></span> Follow</button>
                  </div>
                </div>
                <div class="card mb-4">
                  <div class="card-body">
                    <div class="d-flex align-items-center">
                      <div class="flex-shrink-0" alt="Names"> <img  class="avatar avatar-lg p-1" :src=picture alt="applicant picture"></div>
                      <div class="flex-grow-1 ps-3">
                        <h4 class="mb-0" :names='names'>{{ names }}</h4>
                        <p class="mb-0" :role='role'>{{ role }}</p>
                        <ul class="social-links list-inline mb-0 mt-2">
                          <li class="list-inline-item"><a href="javascript:void(0)" data-bs-toggle="tooltip" data-placement="top" title="" data-bs-original-title="@nathan" aria-label="@nathan"><i class="fab fa-github"></i></a></li>
                          <li class="list-inline-item"><a href="javascript:void(0)" data-bs-toggle="tooltip" data-placement="top" title="" data-bs-original-title="@nathan_andrews" aria-label="@nathan_andrews"><i class="fab fa-twitter"></i></a></li>
                          <li class="list-inline-item"><a href="javascript:void(0)" data-bs-toggle="tooltip" data-placement="top" title="" data-bs-original-title="+420777555987" aria-label="+420777555987"><i class="fa fa-phone"></i></a></li>
                        </ul>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- <form class="card mb-4">
                  <div class="card-header">
                    <h4 class="card-heading">My Profile</h4>
                  </div>
                  <div class="card-body">
                    <div class="row mb-3">
                      <div class="col-auto d-flex align-items-center"> <img  class="avatar avatar-lg p-1" :src=picture alt="applicant picture"></div>
                      <div class="col">
                        <label class="form-label">{{ names }}</label>
                        <input class="form-control" placeholder="Your name">
                      </div>
                    </div>
                    <div class="mb-3"> 
                      <label class="form-label">Bio</label>
                      <textarea class="form-control" rows="8">asd;flnsa Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</textarea>
                    </div>
                    <div class="mb-3"> 
                      <label class="form-label">Email</label>
                      <input class="form-control" placeholder="you@domain.com">
                    </div>
                    <label class="form-label">Password</label>
                    <input class="form-control" type="password" value="password">
                  </div>
                  <div class="card-footer text-end">
                    <button class="btn btn-primary">Save</button>
                  </div>
                </form> -->
              </div>
              <div class="col-lg-8">
                <div class="card overflow-hidden mb-4">
                  <div class="card-header">
                    <h4 class="card-heading">My Profile</h4>
                  </div>
                  <div class="list-group-item border-start-0 border-end-0 py-5">
                      <div class="d-flex">
                        <div class="flex-grow-1 ps-3"><small class="float-right"></small>
                          <h5 class="fw-bold">Bio</h5>
                          <div class="text-muted text-sm" :bio='bio'>{{bio}}</div>
                        </div>
                      </div>
                    </div>
                  <div class="list-group rounded-0">
                    <div class="list-group-item border-start-0 border-end-0 py-5 border-top-0">
                      <div class="d-flex">
                        <div class="flex-grow-1 ps-3"><small class="float-right"></small>
                          <h5 class="fw-bold">Skills</h5>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1 ps-3 text-sm text-muted"><strong class="text-dark">Skill 1 </strong> <br> Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</div>
                          </div>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1 ps-3 text-sm text-muted"><strong class="text-dark">Skill 2 </strong><br>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- <form class="card mb-4">
                  <div class="card-header">
                    <h4 class="card-heading">Edit Profile</h4>
                  </div>
                  <div class="card-body">
                    <div class="row">
                      <div class="col-md-5">
                        <div class="mb-4">
                          <label class="form-label">Company</label>
                          <input class="form-control" type="text" placeholder="Company" value="Names">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-3">
                        <div class="mb-4">
                          <label class="form-label">Username</label>
                          <input class="form-control" type="text" placeholder="Username" value="Names">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-4">
                        <div class="mb-4">
                          <label class="form-label">Email address</label>
                          <input class="form-control" type="email" placeholder="Email">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-6">
                        <div class="mb-4">
                          <label class="form-label">First Name</label>
                          <input class="form-control" type="text" placeholder="First name">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-6">
                        <div class="mb-4">
                          <label class="form-label">Last Name</label>
                          <input class="form-control" type="text" placeholder="Last Name">
                        </div>
                      </div>
                      <div class="col-md-12">
                        <div class="mb-4">
                          <label class="form-label">Address</label>
                          <input class="form-control" type="text" placeholder="Home Address">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-4">
                        <div class="mb-4">
                          <label class="form-label">City</label>
                          <input class="form-control" type="text" placeholder="City">
                        </div>
                      </div>
                      <div class="col-sm-6 col-md-3">
                        <div class="mb-4">
                          <label class="form-label">ZIP</label>
                          <input class="form-control" type="number" placeholder="ZIP">
                        </div>
                      </div>
                      <div class="col-md-5">
                        <div class="mb-4">
                          <label class="form-label">Country</label>
                          <select class="form-control custom-select">
                            <option value="">KE</option>
                            <option value="">UK</option>
                            <option value="">US</option>
                            <option value="">COL</option>
                          </select>
                        </div>
                      </div>
                      <div class="col-md-12">
                        <div class="mb-0">
                          <label class="form-label">About Me</label>
                          <textarea class="form-control" rows="5" placeholder="Here can be your description">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</textarea>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="card-footer text-end">
                    <button class="btn btn-primary" type="submit">Update Profile</button>
                  </div>
                </form> -->
              </div>
            </div>
          </section>
        </div>
        <footer class="footer bg-white shadow align-self-end py-3 px-xl-5 w-100">
          <div class="container-fluid">
            <div class="row">
              <div class="col-md-6 text-center text-md-start fw-bold">
                <p class="mb-2 mb-md-0 fw-bold">© 2021</p>
              </div>
            </div>
          </div>
        </footer>
      </div>
    
</template>
<script>
//importing bootstrap 5 Modules
import "bootstrap/dist/css/bootstrap.min.css";
//import * as Vue from 'vue' // in Vue 3
import axios from 'axios'
// Vue.use(VueAxios, axios)]

export default {
     name: 'App',
     data(){
       return {
         names: '',
         title: '',
         picture: '',
         bio: '',
         role:'',
         //links: [],
       }
     },
     created(){
       axios
       .get("http://torre.bio/api/bios/taniazapata")
       .then(response=>{
         this.names = response.data.person.name;
         this.title = response.data.person.professionalHeadline;
         this.picture = response.data.person.picture
         this.bio = response.data.person.summaryOfBio
         //this.links = response.data.person.links
         this.role = response.data.experiences[0].name
       })
       .catch(error=>{
         console.log('There was an error: ' + error.response);
       })
     }
    //  created(){
    //    axios
    //    .get("https://torre.bio/api/bios/taniazapata")
    //    .then(response=>{
    //      this.names = response.data.person.name;
    //      this.title = response.data.person.professionalHeadline;
    //      this.picture = response.data.person.picture
    //      this.bio = response.data.person.summaryOfBio
    //      //this.links = response.data.person.links
    //      this.role = response.data.experiences[0].name
    //    })
    //    .catch(error=>{
    //      console.log('There was an error: ' + error.response);
    //    })
    //  }
//   methods: {
//     getInfo() {
//       var api = 'https://torre.bio/api/bios/philipmatunda';
//       this.axios.get(api).then((response) => {
//         console.log(response.data)
//       })
//       // or
//       this.$http.get(api).then((response) => {
//         console.log(response.data)
//       })
//     }
//   }
//   mounted() {
//      axios
//     .get('https://torre.bio/api/bios/')
//     .then(response => (this.info = response.data.bpi))
//     .catch(error => console.log(error))
//
}
</script>