<template>
  <div>
    <!-- <h1>{{hihi}}</h1> -->
    <h1>{{ haha }}</h1>
    <button v-on:click="haha = 'Đa click thay doi'">Update Event</button>
    <button v-on:click="destroyEvent">Destroy Event</button>
  </div>
</template>
<script>
export default {
    name: "Lifecycle",
    drops: {
        hihi: String
    },
        data() {
            return{
                haha:"Vue lifecycle"
            }
    },
    beforeCreate() {
        alert('beforeCreate!')
    },
    created(){
        alert('created')
    },
    beforeMount(){
        alert('beforeMount')
    },
    mounted(){
        alert('mounted')
    },
    beforeUpdate(){
        alert('beforeUpdate')
    },
    updated(){
        alert('updated')
    },
    beforeDestroy(){
        alert('beforeDestroy')
    },
    destroyed(){
        alert('destroyed')
    },
    methods:{
        destroyEvent: function(){
            this.$destroy();
        }
    }
}
</script>
<style></style>
