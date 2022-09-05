<template>
  <q-page class="page">
    <div class="enrty">

    </div>
    <div class="results">
      <h3 class="text-center text-white">Natijalar</h3>
      <q-btn @click="screenSize">bos</q-btn>
      <div class="container">
        <div class="card">
          <div class="title text-h6 text-center text-white">Display</div>
          <div class="container">
            <div class="text-white">
              <div>
                eni
              </div>
              <div>
                eni
              </div>
            </div>
            <div class="text-white">
              <div>
                {{screenHeight}}
              </div>
              <div>
                200px
              </div>
            </div>
          </div>
        </div>
        <div class="card"></div>
        <div class="card"></div>
      </div>
    </div>
   
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { ref } from "vue";
export default defineComponent({
  name: "IndexPage",
  setup() {
    const variable = ref(100);
    const px = ref("px");

    const screenHeight = ref('')

    function screenSize(){
      screenHeight.value = screen.height
    }
    

    return {
      screenHeight,
      screenSize,
      variable,
      px,
    };
  },
});
</script>
<style scoped>
.results{
  font-family: 'Popins', sans-serif;
  width: 100%;
  height: 100vh;
  padding: 0;
  position: absolute;
  top: 0;
  left: 0;
  background-image: url("https://catherineasquithgallery.com/uploads/posts/2021-03/1614633626_77-p-kiberpank-fon-dlya-fotoshopa-99.png");
  background-repeat: no-repeat;
  background-size: cover;
}
.container {
  
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}
.card {
  width: 300px;
  height: 400px;
  margin-top: 20px;
  border: 1px solid rgba(255, 255, 255, 0.3);
  background: rgba(41, 39, 39, 0.2);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
}
</style>