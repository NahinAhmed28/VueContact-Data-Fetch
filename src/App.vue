<template>
    <div class="container">
<button class="btn btn-primary" @click="componentToRender='compHome'" >Home </button>
<button  class="btn btn-outline-info" @click="componentToRender='compContact'" >Contact </button>
<button class="btn btn-outline-success" @click="componentToRender='compAbout'" >About </button>


<keep-alive>
<component :is="componentToRender"></component>
   </keep-alive>
    </div>
</template>

<script>
import compHome from './Components/home'
import compAbout from './Components/about'
import compContact from './Components/contact'

export default{
    data() {
        return{
componentToRender:'compHome'
        }
    },
    components: {
        compHome,
        compAbout,
        compContact
    }


}
</script>
