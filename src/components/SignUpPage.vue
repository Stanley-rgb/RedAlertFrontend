<template>
    <v-app>
        <v-content>
            <v-container class="fill-height" fluid>
                <v-row class="align-center justify-center">
                    <v-col cols="12" sm="8" md="8">
                        <v-card class="elevation-12">
                            <v-window v-model="step">
                                <v-window-item :value="1">
                                    <v-row>
                                        <v-col cols="12" md="8">
                                            <v-card-text class="mt-5">
                                                <h3 class="text-center display-1 deepRed--text text--accent-2"> Login</h3>
                                                <!--<div class="text-center" mt-4>
                                                    <v-btn class="mx-2" fab color="black" outlined>
                                                        <v-icon>fab fa-facebook-f</v-icon>
                                                    </v-btn>
                                                    <v-btn class="mx-2" fab color="black" outlined>
                                                        <v-icon>fab fa-google-plus-g</v-icon>
                                                    </v-btn>
                                                </div>-->
                                                <v-form>
                                                    <v-text-field
                                                    label="Email"
                                                    name="Email"
                                                    prepend-icon="email"
                                                    type="text"
                                                    color="teal accent-3"
                                                    />

                                                    <v-text-field
                                                    id="password"
                                                    label="Password"
                                                    name="Password"
                                                    prepend-icon="lock"
                                                    type="password"
                                                    color="teal accent-3"
                                                    />
                                                </v-form>
                                            </v-card-text>
                                            <div class="text-center mt-3 ">
                                                <v-btn rounded color="deepRed accent-3" dark>login</v-btn>
                                            </div>
                                            <div class="mt3 text-right">
                                                <router-link to="forgot">forgot password ?</router-link>
                                                <!--<h3 class="text-right" link>forgot password ?</h3>-->
                                             </div>
                                        </v-col>
                                        <v-col cols="12" md="4" class="deepRed accent-3">
                                            <v-card-text class="white--text mt-12">
                                                <h1 class="text-center display-1">Red Alert</h1>
                                                <h5 class="text-center">To Report a case please fill in your datails and sign up.</h5>
                                            </v-card-text>
                                            <div class="text-center">
                                                <v-btn rounded outlined="" dark @click="step++">SIGN UP</v-btn>
                                            </div>
                                        </v-col>
                                    </v-row>
                                </v-window-item>
                                <v-window-item :value="2">
                                    <v-row class="fill-height">
                                        <v-col cols="12" md="4" class="deepRed accent-3">
                                            <v-card-text class="white--text mt-12">
                                                <h1 class="text-center display-1"> Welcome Back </h1>
                                                <h5 class="text-center">Please login to your account to post a red alert</h5>
                                            </v-card-text>
                                            <div class="text-center">
                                                <v-btn rounded outlined="" dark @click="step--">SIGN IN</v-btn>
                                            </div>
                                        </v-col>
                                        <v-col cols="12" md="8">
                                            <v-card-text class="mt-5">
                                                <h1 class="text-left display-1 deepRed--text text--accent-2"> Create Account</h1>
                                                <v-form>
                                                    <v-layout class="text-center">
                                                        <v-flex xs6>
                                                            <v-text-field v-model="firstName"
                                                                label="First Name"
                                                                name="First Name"
                                                                prepend-icon="person"
                                                                type="text"
                                                                color="teal accent-3"
                                                            />
                                                        </v-flex>
                                                        <v-flex xs6>
                                                            <v-text-field v-model="lastName"
                                                                label="Last Name"
                                                                name="Last Name"
                                                                prepend-icon="person"
                                                                type="text"
                                                                color="teal accent-3"
                                                            />
                                                        </v-flex>
                                                    </v-layout>
                                                    
                                                            <v-text-field v-model="emailAddress"
                                                                label="Email"
                                                                name="Email"
                                                                prepend-icon="email"
                                                                type="text"
                                                                color="teal accent-3"
                                                            />
                                                        
                                                            <v-text-field v-model="phoneNo"
                                                                label="Phone Number"
                                                                name="Phone Number"
                                                                prepend-icon="phone"
                                                                type="text"
                                                                color="teal accent-3"
                                                            />
                                                       
                                                    <v-text-field v-model="password"
                                                        id="password"
                                                        label="Password"
                                                        name="Password"
                                                        prepend-icon="lock"
                                                        type="password"
                                                        color="teal accent-3"
                                                    />

                                                    <v-text-field
                                                        id="re-password"
                                                        label="Re-Enter Password"
                                                        name="Re-Enter Password"
                                                        prepend-icon="lock"
                                                        type="password"
                                                        color="teal accent-3"
                                                    />
                                                </v-form>
                                            </v-card-text>
                                            <v-checkbox label="I have read and agree to 'Red Alert' User Agreement and Privacy policy."></v-checkbox>
                                            <div class="text-center">
                                                <v-btn rounded color="deepRed accent-3" dark v-on:click="signUp">Create Account</v-btn>
                                            </div>
                                                <h4 class="text-center deepRed--text text--accent-1"> OR </h4>
                                                <v-layout class="text-center">
                                                
                                                <v-flex xs6>
                                                    <div class="text-left  mt-4">
                                                        <p class="text-center mt-n2"><v-icon>fab fa-google-plus-g</v-icon>  Sign Up with Google</p>
                                                    </div>
                                                </v-flex>

                                                <v-flex xs6>
                                                    <div class="text-left mt-4">
                                                        <p class="text-center mt-n2"><v-icon>fab fa-facebook-f</v-icon>  Sign Up with Facebook</p>
                                                    </div>
                                                </v-flex>

                                        </v-layout>
                                        </v-col>
                                    </v-row>
                                </v-window-item>
                            </v-window>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-content>
    </v-app>
</template>
<script>
import axios from 'axios'
export default{  
    data: () =>({
        step: 1,
        
            firstName:'',
            lastName:'',
            emailAddress:'',
            phoneNo:'',
            password:''

        
       
        
    }),
    methods:
    {
        
            async signUp()
            {
                //console.warn(this.email)
                let result = await axios.post("http://192.168.74.144:8081/api/v1/user/add",{
                    firstName:this.firstName,
                    lastName:this.lastName,
                    emailAddress:this.emailAddress,
                    phoneNo:this.phoneNo,
                    password:this.password
                    
                });
                //console.log(result);
                //alert(result.data.message);
                if(result.data.statusCode == 201)
                {
                    //alert("sign up success");
                }
            }
    },
    props: {
        source: String
    },
    
}

</script>
