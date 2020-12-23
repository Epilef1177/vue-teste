<template>
    <div class="body" >
        <div class="login">
            <h1>Login</h1>
            <input v-model="name" type="text" placeholder="Name or E-mail"/> <br/>
            <input v-model="password" type="text" placeholder="PassWord"/> <br/>
            <button @click="verify()">Login</button>
        </div>
        <section class="loged">
            {{enable}}
        </section>
        <p v-if="enable == 'silver' || enable == 'gold' || enable == 'diamond'">Silver</p>
        <p v-if="enable == 'gold' || enable == 'diamond'">Gold</p>
        <p v-if="enable == 'diamond'">Diamond</p>
    </div>
</template>

<script>
export default {
    name: 'login',
    data(){
        return {
            name: "",
            password: "",
            enable: "",
            profiles: [
                {
                    name: "profile-silver",
                    password: "123",
                    enable: "silver",
                },
                {
                    name: "profile-gold",
                    password: "123",
                    enable: "gold",
                },
                {
                    name: "profile-diamond",
                    password: "123",
                    enable: "diamond",
                },
            ]
        }    
    },
    methods: {
        verify: function(){
            let ok = false;
            for (let i = 0; i < 3; i++){
                ok = false;
                if(this.profiles[i].name == this.name){
                    ok = true;
                }
                if(this.profiles[i].password == this.password && ok){
                    this.enable = this.profiles[i].enable;
                    this.$emit("loged",{
                        enable: this.enable,
                    })
                }
            }
        },
    },
    
}
</script>

<style scoped>
    .body {
        min-height: 500px;
    }
    .login {
        margin: 0px auto 0px auto;
        padding: 5px;
        text-align: center;
        border: solid 2px black;
        width: 40%;
    }
    input, button {
        margin-top: 15px;
    }
    
</style>