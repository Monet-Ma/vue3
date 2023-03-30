<template>
  <div class="hello"
       ref="editFormRef"
       :model="account_form">
    <div class="bl">
      <p>虚妄时装</p>
      <input class="inp" type="number" v-model="ssp_dress" />
    </div>
    <div class="bl">
      <p>稀世时装</p>
      <input class="inp" type="number" v-model="sp_dress" />
    </div>
    <div class="bl">
      <p>奇珍时装</p>
      <input class="inp" type="number" v-model="dress" />
    </div>
    <div class="bl">
      <p>角色数</p>
      <input class="inp" type="number" v-model="roles" />
    </div>
    <div class="bl">
      <p>随从数量</p>
      <input class="inp" type="number" v-model="retinue" />
    </div>
    <div class="bl">
      <p>虚妄随身物品</p>
      <input class="inp" type="number" v-model="ssp_goods" />
    </div>
    <div class="bl">
      <p>稀世随身物品</p>
      <input class="inp" type="number" v-model="sp_goods" />
    </div>
    <div class="bl">
      <p>奇珍随身物品</p>
      <input class="inp" type="number" v-model="goods" />
    </div>
    <div class="bl">
      <p>头像</p>
      <input class="inp" type="number" v-model="head" />
    </div>
    <div class="bl">
      <p>头像框</p>
      <input class="inp" type="number" v-model="head_frame" />
    </div>
    <div class="bl">
      <p>涂鸦</p>
      <input class="inp" type="number" v-model="graffiti" />
    </div>
    <div class="bl">
      <p>等待动作</p>
      <input class="inp" type="number" v-model="waiting_action" />
    </div>
    <div class="bl">
      <p>个性动作</p>
      <input class="inp" type="number" v-model="pursue_action" />
    </div>
    <div class="bl">
      <p>追击音乐</p>
      <input class="inp" type="number" v-model="music" />
    </div>
    <div class="bl">
      <p>归宿分</p>
      <input class="inp" type="number" v-model="score" />
    </div>
    <div class="bl">
      <p>平台</p>
      <input class="inp" type="text" v-model="platform" />
    </div>
    <div class="bl">
      <p>上架售价</p>
      <input class="inp" type="number" v-model="price" />
    </div>
    <div class="bl blbtn">
      <button class="btn" @click="clk"> Predict</button>
    </div>
  </div>
</template>

<script>
//
//import {reactive} from "vue";
import axios from "axios";

// const account_form = reactive({
//   ssp_dress: "",
//   sp_dress: "",
//   dress: "",
//   roles: "",
//   retinue: "",
//   ssp_goods: "",
//   sp_goods: "",
//   goods: "",
//   head: "",
//   head_frame: "",
//   graffiti: "",
//   waiting_action: "",
//   pursue_action: "",
//   music: "",
//   score: "",
//   platform:"",
//   price:"",
// })
const submitForm = () => {
  axios.post('http://localhost:5000', 'hello').then(() => {

  })
}
// const item_form = () => {
//     axios.get("http://127.0.0.1:5000/",).then(res => {
//       console.log(res.data)
//   })
// }
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  methods:{
    clk(){
      // alert("账号预估价值为：19697.91674")
      submitForm()
      // item_form()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content:space-between;
  padding: 0 200px 0 200px;
}
.bl{
  display: flex;
  margin: 10px 70px 0px 70px;
  width :500px;
  justify-content:space-between;
  align-items: center;
  p{
    font-family: STXingkai;
    font-size: 32px;
    color: #efefef;
    width:220px;
    margin:15px;
  }
  .btn{
    background: rgba(255,255,255,0.15);
  }
}
.blbtn{
  justify-content: center;
}
.inp {
  font-family: 'Montserrat', sans-serif;
  letter-spacing: -0.2px;
  width:200px;
  height:50px;
  background: rgba(255,255,255,0.15);
}

h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}


</style>
