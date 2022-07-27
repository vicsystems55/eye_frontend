<template>
    <div>
        <Breadcrumbs main="Members" title="Member"/>
        <!-- Container-fluid starts-->
        <div class="container-fluid">
            <div class="row">
              <div class="col-md-12">
                <div class="card">
                    <div class="card-header">
                      <h5 class="card-title">{{user.name}}</h5>
                    </div>
                    <div class="card-body">
                     
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
        loading: false,
        user: []
      };
    },

    methods: {
      getUser(){

        // alert(this.$route.params.id)

        this.loading = true

                  axios({
                    method: "get",
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

      }
    },

    mounted() {
      this.getUser()
    },
  };
</script>