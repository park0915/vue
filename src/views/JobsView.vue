<template>
    <div>
        <div v-for = "job in this.$store.state.jobs ">{{job.title}}</div>
        <!--<div v-for = "user in jobs">{{jobs.title}}</div>-->
    </div>
</template>

<script>
    export default {
        created(){
            this.$store.dispatch('FETCH_JOBS')
        }

    }
/*import {fetchJobsList} from '../api/index';

    export default {
        data(){
            return{
                jobs: []
            }
        },
        created(){
            fetchJobsList()
                .then(response => {
                    console.log(response.data)
                    this.jobs = response.data
                })
                .catch(error => console.log(error))
         }
    }
*/
</script>

<style scoped>

</style>