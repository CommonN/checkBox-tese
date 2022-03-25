<template>
  <div class="q">
      <div class="w"> 
              <ul class="t">
                  <li><input type="checkbox" v-model="checkAll"><span>全选</span></li>
                  <li v-for="(obj,index) in arr " :key="index">
                      <input type="checkbox" v-model="obj.c">
                      <span>{{obj.name}}</span></li> 
              </ul>
      </div>
  </div>
</template>

<script>
export default {
data () {
    return {
        
        arr:[
            {
                name:'aaa',
                c:false
            },
             {
                name:'bbb',
                c:false
            },
             {
                name:'ccc',
                c:false
            },
             {
                name:'ddd',
                c:false
            },
             {
                name:'eee',
                c:false
            },
             {
                name:'fff',
                c:false
            }
        ]
    }
},
computed: {
    checkAll:{
        set(val){
           this.arr.forEach(obj => obj.c = val)
        },
        get(){
          return this.arr.every(obj => obj.c ===true)
        }
       
    }
}
}
</script>

<style lang='less'>
 .q{
    width: 290px;
    height: 240px;
    padding-top: 10px;
    border: 1px solid  #ccc ;
    .w{
        width: 260px;
        height: 230px;
        margin:  auto;
        border: 1px solid  #ccc ;
        border-radius: 5px;
         .t{
            display: flex;
     
            flex-wrap: wrap;
            
            // justify-content:space-around;
            li{
                width:33.33%;
            }
            
            
        }
        
    }
    
}
</style>