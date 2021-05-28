<template>
  <div>
    <v-card dark>
      <div id="contactMain">
        <h1 align="center" id="title">Contact</h1>
        <v-container style="max-width: 800px;">
          <fade-in-component>
            <section>
              <v-card elevation="8">
                <v-card-text>
                  <v-container>
                    <v-row>
                      <v-col cols="12">
                        <v-text-field label="お名前" required v-model="name"></v-text-field>
                      </v-col>
                      <v-col cols="12">
                        <v-text-field label="メールアドレス" required v-model="email"></v-text-field>
                      </v-col>
                      <v-col cols="12">
                        <v-textarea label="問い合わせ内容" outlined required v-model="description"></v-textarea>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn  v-on:click="submit" color="primary">Send</v-btn>
                </v-card-actions>
              </v-card>
            </section>
          </fade-in-component>
        </v-container>
      </div>
      <div id="copyRight">
        <h5 align="center">icon by <a href="https://twitter.com/MelvilleTw" target="_blank" rel="noopener noreferrer">@V_Melville</a></h5>
        <h4 align="center">© 2021 Genshi0916</h4>
      </div>
    </v-card>
  </div>
</template>
<script>
  import FadeInComponent from '../components/FadeInComponent'
  export default{
    components:{
      FadeInComponent,
    },

    data:()=>({
      dialog:true,
      name:'',
      email:'',
      description:''
    }),

    methods:{
      submit:function(){
        var name = this.name
        var email = this.email
        var description = this.description
        const payload = {
          text: '問い合わせがありました\n'+
                '名前:'+name+'\n'+
                'email:'+email+'\n'+
                '内容:'+description+'\n'
        }
        const url = 'ここにはwebhookのurlが入る'

        fetch(url,{
          method:'POST',
          body:JSON.stringify(payload)
        }).then(()=>{
          alert('送信完了\n折り返しの連絡をお待ちください');
          this.name="";
          this.email="";
          this.description="";
        })
      }
    }
  }
</script>
<style scoped>
  #contactMain{
    padding-bottom: 30px;
  }

  #title{
    padding:20px 0px;
  }

  #copyRight{
    padding:20px 0px;

  }

/* aタグのデコレーションを消す */
  a{
    text-decoration: none;
  }
</style>
