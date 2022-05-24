<template>
    <div>
        <!-- <h1>Template in vue js</h1> -->
        <p v-html="rowHtml"></p>
        <h3 v-once>{{ name }}</h3>
        <h3>{{ name }}</h3>
        <h3>{{ a+b}}</h3>
        <h3>{{ ok?"Yes":"No"}}</h3>
        <button v-bind:disabled="disableBtn" v-on:click="updateText">Click me</button>
    </div>
</template>
<script>
export default{ 
    name: 'vue-home',
    data(){
        return{ 
            name: 'Vijaykumar',
            a:10,
            b:20,
            ok:false,
            rowHtml:"<h1>Template in vue js</h1>",
            disableBtn: false
        }
    },
    methods:{ 
        updateText(){
            // this.name="Vijay"
            this.ok=!this.ok
        }
    }
}
</script>