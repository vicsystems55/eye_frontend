<template>
    <div>
        <Breadcrumbs main="Dashboard" title="Profile"/>
        <!-- Container-fluid starts-->
        <div class="container-fluid">
            <div class="row">
              <div class="col-md-12">
                <div class="card">
                    <div class="card-header">
                      <h5 class="card-title">Profile</h5>
                    </div>
                    <div class="card-body">

                      <div class="row">
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Name</label>
                            <input type="text" class="form-control" v-model="name">
                          </div>

                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Email</label>
                            <input type="text" class="form-control" v-model="email">
                          </div>

                        </div>

                        <div class="col-md-6">
                          <label class="">Gender</label>
                          <div class="m-t-15 m-checkbox-inline custom-radio-ml">
                          <div class="form-check form-check-inline radio radio-primary">
                            <input class="form-check-input" id="radioinline1" type="radio" v-model="gender" :value="male" data-bs-original-title="" title="">
                            <label class="form-check-label mb-0" for="radioinline1">Male</label>
                          </div>
                          <div class="form-check form-check-inline radio radio-primary">
                            <input class="form-check-input" id="radioinline2" type="radio" v-model="gender" :value="female" data-bs-original-title="" title="">
                            <label class="form-check-label mb-0" for="radioinline2">Female</label>
                          </div>
                          </div>

                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Phone</label>
                            <div class="d-flex justify-content-start">
                              <select type="text" class="form-control col-4">
                                <option value="">+234 (NG)</option>
                                <option value="">+234 (NG)</option>

                                <option value="">+234 (NG)</option>

                                <option value="">+234 (NG)</option>

                              </select>
                              <input type="text" class="form-control">
                            </div>
                          </div>

                        </div>

                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Bio</label>
                            <textarea rows="5" v-model="bio" type="text" class="form-control" placeholder="A brief about yourself"></textarea>
                          </div>

                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Address</label>
                            <textarea rows="5" v-model="address" type="text" class="form-control" placeholder="Your address"></textarea>
                          </div>

                        </div>

                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Facebook <span class="text-muted">(optional)</span></label>
                            <input type="text" class="form-control" placeholder="your facebook url">
                          </div>

                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Twitter <span class="text-muted">(optional)</span></label>
                            <input type="text" class="form-control" placeholder="">
                          </div>

                        </div>

                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Youtube <span class="text-muted">(optional)</span></label>
                            <input type="text" class="form-control" placeholder="">
                          </div>

                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">LinkedIn <span class="text-muted">(optional)</span></label>
                            <input type="text" class="form-control" placeholder="">
                          </div>

                        </div>

                        <div class="col-md-6">
                              <div class="form-group">
                                  <label for="">Language Preference</label>
                                  <select v-model="language" name="language" id="" class="form-control">
                                      
                                      <option :value="''">--Select Language--</option>
                                      <option :value="'English'">English</option>
                                      <option :value="'French'">French</option>
                                      <option :value="'Others'">Others</option>
                                  </select>
                              </div>
                        </div>
                        <div class="col-md-6">
                                  <div class="form-group">
                                        <label for="">Highest Level of Education</label>

                                  <select class="form-control" name="level_education" >
                                      <option value=""></option>
                                      <option value="O Levels">O Levels</option>
                                      <option value="Degree">Degree</option>
                                      <option value="Masters">Masters</option>
                                      <option value="Others">Others</option>
                                  </select>
                                  
                              </div>

                        </div>


                        <div class="col-md-6">
                            <div class="form-group">
                              <label for="">Do you you have an existing business?</label>

                              <select class="form-control" name="existing_business" value="">
                                  <option value="Yes">Yes</option>
                                  <option value="No">No</option>
                              </select>
                              
                          </div>
                        </div>
                        <div class="col-md-6">
                                      <div class="form-group">
                                        <label for="">Business Name (or Proposed)</label>
                                        <input 
                                        type="text"  
                                        class="form-control shadow" 
                                        name="business_name" 
                                        value="">
                                        
                                    </div>
                        </div>
                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">Is your business registered?</label>

                            <select class="form-control" name="business_registration_status" id="">
                                <option value="Yes">Yes</option>
                                <option value="No">No</option>
                            </select>
                            
                        </div>

                        </div>
                        <div class="col-md-6">
                                    <div class="form-group">
                                        <label for="">Describe Your Business, and What differenciates it from its Competitors.</label>

                                        <textarea type="text" rows="3" cols="10" 
                                        placeholder="e.g My is business within the fashion sphere, I make cloths for males and females"
                                        name="business_description" 
                                        class="form-control"></textarea>
                                        
                                    </div>
                        </div>

                        <div class="col-md-6">
                          <div class=" animate-chk">
                            <label for="">Which three (3)  areas do you have a problem with in your Business?</label>                            
                            <div class="row">
                              <div class="col">
                                <label class="d-block" for="chk-ani">
                                  <input class="checkbox_animated" id="chk-ani" type="checkbox" checked="" data-bs-original-title="Human Resources" title="">Human Resources
                                </label>
                                <label class="d-block" for="chk-ani1">
                                  <input class="checkbox_animated" id="chk-ani1" type="checkbox" data-bs-original-title="" title="">Branding
                                </label>
                                <label class="d-block" for="chk-ani2">
                                  <input class="checkbox_animated" id="chk-ani2" type="checkbox" checked="" data-bs-original-title="" title="">Legal Issues
                                </label>
                                <label class="d-block" for="chk-ani3">
                                  <input class="checkbox_animated" id="chk-ani3" type="checkbox" data-bs-original-title="" title="">Business Partnership
                                </label>
                                <label class="d-block" for="chk-ani">
                                  <input class="checkbox_animated" id="chk-ani" type="checkbox" checked="" data-bs-original-title="" title="">Sales
                                </label>
                              </div>
                              <div class="col">
                                <label class="d-block" for="chk-ani1">
                                  <input class="checkbox_animated" id="chk-ani1" type="checkbox" data-bs-original-title="" title="">Insurance
                                </label>
                                <label class="d-block" for="chk-ani2">
                                  <input class="checkbox_animated" id="chk-ani2" type="checkbox" checked="" data-bs-original-title="" title="">Marketing
                                </label>
                                <label class="d-block" for="chk-ani3">
                                  <input class="checkbox_animated" id="chk-ani3" type="checkbox" data-bs-original-title="" title="">Finance Module
                                </label>
                                <label class="d-block" for="chk-ani3">
                                  <input class="checkbox_animated" id="chk-ani3" type="checkbox" data-bs-original-title="" title="">Risk Management
                                </label>
                              </div>
                            </div>
                          </div>
                        </div>

                        <div class="col-md-6">
                            <div class="form-group">
                              <label for="">Are You in Partnership?</label>

                              <select class="form-control" name="in_partnership" id="">
                                  <option value="Yes">Yes</option>
                                  <option value="No">No</option>
                                
                                  
                              </select>
                              
                          </div>

                            <div class="form-group">
                              <label for="">Are You Actively Seeking a Co-Founder?</label>

                              <select class="form-control" name="seeking_cofounder" id="">
                                  <option value="Yes">Yes</option>
                                  <option value="No">No</option>
                                
                                  
                              </select>
                              
                          </div>
                        </div>


                        <div class="col-md-6">

                          <div class="form-group">
                            <label for="">What Industry Would You Like to Launch a Business?</label>

                              <select class="form-control" name="business_industry" id="">

                                  <option value="Manufacturing">Manufacturing</option>
                                  <option value="Textiles">Textiles</option>
                                  <option value="Agriculture">Agriculture</option>
                                  <option value="Technology ">Technology </option>
                                
                                  
                              </select>
                              
                          </div>

                          <div class="form-group">
                              <label for="">What Do You Hope to gain from This Programme?</label>
                              <textarea rows="5" type="text" placeholder="I will like to be able to gather the knowledge needed to kick start my business." name="hope_to_gain" value="" class="form-control"></textarea>

                          </div>

                        </div>

                        <div class="col-md-6">
                          <div class=" animate-chk">
                            <label for="">Are any of the Following Challenges Keeping You from starting a Business?</label>                            
                            <div class="row">
                              <div class="col-12">
                                <label class="d-block" for="chk-ani">
                                  <input class="checkbox_animated" id="chk-ani" type="checkbox" checked="" data-bs-original-title="Human Resources" title=""> I don’t want to quit my job
                                </label>
                                <label class="d-block" for="chk-ani1">
                                  <input class="checkbox_animated" id="chk-ani1" type="checkbox" data-bs-original-title="" title="">I don’t have a great idea yet
                                </label>
                                <label class="d-block" for="chk-ani2">
                                  <input class="checkbox_animated" id="chk-ani2" type="checkbox" checked="" data-bs-original-title="" title="">I am paying off loans
                                </label>
                                <label class="d-block" for="chk-ani3">
                                  <input class="checkbox_animated" id="chk-ani3" type="checkbox" data-bs-original-title="" title="">I hope to work for a startup first
                                </label>
                                <label class="d-block" for="chk-ani">
                                  <input class="checkbox_animated" id="chk-ani" type="checkbox" checked="" data-bs-original-title="" title="">I want to find a Co-Founder
                                </label>
                                <label class="d-block" for="chk-ani1">
                                  <input class="checkbox_animated" id="chk-ani1" type="checkbox" data-bs-original-title="" title="">I am still in school
                                </label>
                                <label class="d-block" for="chk-ani2">
                                  <input class="checkbox_animated" id="chk-ani2" type="checkbox" checked="" data-bs-original-title="" title=""> I am struggling to choose between a few ideas
                                </label>
                              
                              </div>
                              
                            </div>
                          </div>  
                          
                          <div class="form-group">
                              <label for="">Any Other Challenges?</label>
                              <input type="text" name="other_challenges" value="" class="form-control">

                          </div>

                        </div>

                        <div class="col-md-12 py-">
                          <div class="col-md-4 mx-auto">

                            <button v-if="loading" class="btn btn-primary btn-lg btn-block" disabled>Submitting...</button>

                            <button v-else class="btn btn-primary btn-lg btn-block">Submit</button>

                          </div>
                        </div>






                      </div>
                    
                    </div>
                </div>
              </div>

            </div>
        </div>
        <!-- Container-fluid Ends-->
    </div>
</template>

<script>
  import { VueEditor } from 'vue2-editor';
  import axios from 'axios'

  export default {
    components: {
      VueEditor
    },
    data() {
      return {
        content: '<h1>Some initial content</h1>',

        name: '',
        email:'',

        gender: '',
        dob: '',
        country: '',
        state: '',
        address: '',
        phone: '',
        social_link: '',
        bio: '',
        language: '',
        level_education: '',
        existing_business: '',
        business_name: '',
        business_registration_status: '',
        years_in_business: '',
        gross_revenue: '',
        industry: '',
        business_description: '',
        business_problems: '',
        in_partnership: '',
        seeking_cofounder: '',
        business_industry: '',
        challenges: '',
        other_challenges: '',
        hope_to_gain: '',

        loading: false

      };
    },

    methods: {
      getProfile(){



                  axios({
                    method: "get",
                    url: process.env.VUE_APP_URL+'/api/users',
                    headers: {
                        'Access-Control-Allow-Origin': '*',
                        'Content-type': 'application/json',
                        'Accept': 'application/json',
                        'Authorization': 'Bearer ' +localStorage.getItem('user_token')

                    },

                    })
                    .then( (response) =>{

                      this.loading = false
                        //handle success

                      this.user = response.data


                      this.name = response.data.name
                      this.email = response.data.email



                      console.log(response);


                    })
                    .catch( (response)=> {

                      this.loading = false

                      console.log(response);

                    });
      },
      updateProfile(){


        this.loading = true

                  axios({
                    method: "post",
                    url: process.env.VUE_APP_URL+'/api/users',
                    params: {
                       usercode: this.$route.params.id
                    },
                    headers: {
                        'Access-Control-Allow-Origin': '*',
                        'Content-type': 'application/json',
                        'Accept': 'application/json',
                        'Authorization': 'Bearer ' +localStorage.getItem('user_token')

                    },

                    })
                    .then( (response) =>{

                      this.loading = false
                        //handle success

                      this.user = response.data

                      console.log(response);


                    })
                    .catch( (response)=> {

                      this.loading = false

                      console.log(response);

                    });
      },


    },

    mounted() {
      this.getProfile()
    },
  };
</script>