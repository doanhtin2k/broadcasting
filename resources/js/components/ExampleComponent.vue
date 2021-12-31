<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                    </div>
                    <button class="btn btn-primary" @click="change('en')">English</button>
                    <button class="btn btn-primary" @click="change('vi')">Việt Nam</button>
                    {{$t("welcomeMsg")}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import i18n from './../plugins/i18n';
    export default {        
        mounted() {
           
        },
        data() {
            return {
                 name: this.$t("welcomeMsg")
            }
        },
        methods: {
            change(languge){
                console.log(languge);
                 i18n.locale = languge;
                 this.name = this.$t("welcomeMsg")
            }
        }
        
    }
</script>
