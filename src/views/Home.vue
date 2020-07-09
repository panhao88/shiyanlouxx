<template>
 <div>
   <div class="box">
     <head1></head1>
     <Rotation :arr='arr' :app='app' v-if="arr.length > 0" > </Rotation>
     <lou :akk='akk' v-if="akk.length > 0">
       <template #to>
          课程分类
       </template>
       <template #do>
         我是你爸爸
       </template>
     </lou>
     <jingxuan :abb= 'abb'>
       <template>
        
       </template>
       <template>
         
       </template>
     </jingxuan>
   </div>
 </div>
</template>

<script>
import axios from 'axios'
import head1 from '../components/head1'
import Rotation from '../components/Rotation'
import lou from '../components/lou'
import jingxuan from '../components/jingxuan'
 export default {
   name: '',
   props: {
   },
   components: {
     head1,
     Rotation,
     lou,
     jingxuan,
   },
   data () {
     return {
       arr:[],
       abb:[],
       app:[],
       akk:[]
     }
   },
   methods: {
     getData(){
       axios.get('http://120.78.14.107/api/v2/index/banner-pictures').then(res => {
         if(res.data.length > 0){
           this.arr = res.data
          }
          // console.log(res.data);
       }).catch(err => {
         console.log(err);
       })
     },
     getTOdo(){
       axios.get(' http://120.78.14.107/api/v2/index/classfication-courses').then( res=> {
         this.abb = res.data
        //  console.log(res.data);
       }).catch(err => {
         console.log(err);
       })
     },
     getHaha(){
       axios.get('http://120.78.14.107/api/v2/index/categories').then(res => {
         this.app = res.data
         console.log(res.data);
       }).catch( err => {
         console.log(err);
       })
     },
     getKodo(){
       axios.get(' http://120.78.14.107/api/v2/index/louplus').then(res => {
         this.akk = res.data
        //  console.log(res.data);
       }).catch(err => {
         console.log(err);
       })
     }
   },
   mounted() {
     this.getData()
     this.getTOdo()
     this.getHaha()
     this.getKodo()
    },
   watch: {

   },
   computed: {

   },
   filters: {

   },
 }
</script>

<style scoped lang='scss'>
  .box{
    // width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>