<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Base64ToFile from "dvs-base64tofile";
export default {
  name: 'app',
  data() {
    return {
      temp:
        "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACMAAAAjCAYAAAAe2bNZAAAAAXNSR0IArs4c6QAABQxJREFUWAmtWDtPW0kUHhsbjHljC4QRCCJB8gc2qSJtijSrRSJSUiVlijQpoySstF2kRJHSpUqZ7Gq12iIk6dKgjbagjagoQAjWNm/EG8xjv2/kM5o7vtw7sBzp6sydOTPnu2e+c2bshDqHnJ6epnd2dm4lEokRtK9iagG6gPcMdAnvRbTnob82NTV9QXv5HMurhI/x/v7+laOjo1/hcBT2bT5zAOQE9v8kk8nXAPbZa06UERbL7+7uEsQjPOko25ixb3V1dU+y2exklN2ZkQGI6ycnJx8BoidsAYwpREsdHx8rtlOplIJDrcPsGSn0jzU3N78KG2dfKJjt7e0HGHsHIBl7Ip1jTG1tbam9vT17yLTr6+sVtkW1tLSoTCYwXdsA1G8Yfwi9byZVGzVgCAQg3tuG/PL19XX9sO0rBJTL5RQB2gIgnwFotBotMxQAg625AWcTdkQODw9VsVhU1BcROFTd3d2qtbU1MB39L7Flz+1OAwYA8kjb79CGIwCnSqWS5oU96SLtzs5Olc/nA1PBsXsg9V/SmZRGNWsMEEbisoDQx9ramtrY2BB3WmMX3ti7oMGwjqDzkViSF9waZsplytLSUoD48NmH3XgsPjSYakEzdYRkvShHZOGz9OLiYmAIgMbwZNmZRCON545YMH0JxldQYVVjY6Oi9hF+5Obmpm3aDorcZkeKZw20oTrriE/6ssANDg7qeiIrr6ysqPl5Hk3RQu7Y2YVg8JgZTyHFeOiZ2QQTJ0zXoaEhValU1NTUlOZWW1ubGhgY0FWZxI8ScFTbsWpT4P9nam7TNTYojAjTOU46Ojp02Z+ZmdGAOI9bu7y8rJjCPuL4yQNHjtBMOpMvPsJ6sbq6yi8KmC8sLCg+PsKo2gK6FFJYsCCdvqlMwjIrULB0uac+ODjQkcGislykDvnwQhL7b04zH+Iya0henjf9/f26bnB7yKPh4WHV3t4eCUIG3agSBzlj2CaEkglhmkAoXV1danp6WjGDWF1nZ2d1yvb19YVNq+lzfQFMicWhKJbiSN7DNMPLryJh3UgSVDqdrjmlw9ZxwcCmyG0yhYEG7nHvLkQgBBTGLyGlTwG07zrAUAEPy4zMV9shL0ZxwqjYRUvsmdaMFutIlPCjbTCwnQCgoySc8xZvbky8EMUJCcsM6u3tNccAicv6wwM2TlwfiPY45+j7DK6Rf6N9UxZhBeXVMkqY3jwOGhoaTL3hPPcgdNfgFnKe8BOBOEVfPz5uQYNBbRhBeD/JRB5mc3Nzxon0h2mGnE/c1shcFky7SgPM77jx3ee4BsOGGx2erOVymUOXJuQjt1YEQA4RoWuI8iz7zLmPzic2d0hQ+wtkgYtqbmdPjzl5ZJm3AoQdJjJ8wYn9FGR6ybYIj3ve0P6PMCIEYqc8PnwS/T9Cm9QLgKFDAPoAQHoPBQB/I5GY57390Tmj60YYAP7F8wPAmOpPXzVgACQDQv8JPSJgRJNHjFQcWUlopi9BSNbIGgSC9k8g7XfpE10DhgMAkgSgF9DPxNDWrMC8j7DiyvEgWcVi5hQ0MxVAJvHccSMiBqFgZBAO7yLl+XPC7/STiY4GAP4CfAsQY2gbjjhmtdvkGgAIt+0x9BjG/O4H1UXgmLevP7BVv9hZ4/qQ98jIiBE1wGQRqdvQo3h4Zw3+PKwaA0AFzQnYjAPEOCtrdShWeYNxV4KzHCLGW6L+5wog9D9XiEAZbb/7q7Pof18Sk5wTxuUzAAAAAElFTkSuQmCC"
    };
  },
  components: {
    HelloWorld
  },

  mounted() {
    // base64ImageToFile(base64Image, "/tmp/", function(err) {
    //   if (err) {
    //     return console.error(err);
    //   }
    //   console.log(imgPath);
    // });
  
    new Base64ToFile(this.temp, "image/png").save();
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
