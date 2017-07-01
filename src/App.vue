<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="appColor='appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="appColor='appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="appColor='appRed'" >Load Red Template</button>
                <hr>
                <component v-bind:is="appColor">
                    <p>This is content!</p>
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        },

        data: function(){
            return{
                appColor: 'appBlue',
            }
        }
    
    }
</script>

<style>
</style>
