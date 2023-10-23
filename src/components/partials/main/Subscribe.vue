<script>
  export default {
    name: 'Subscribe',

    data(){
      return{
        title: 'Subscribe Now To Our Newsletter',
        email: 'Email address...',
        icon: 'fa-solid fa-paper-plane'
      }
    }
  }
</script>

<template>
  <section class="subscribe">
    <div class="container">
      <h3>{{ title }}</h3>

      <div class="email">
        <input type="email" :placeholder="email">

        <div class="send">
          <i :class="icon"></i>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .subscribe{
    padding: 50px 0;
    background-color: $bg-red;

    .container{
      display: flex;
      justify-content: space-between;
      align-items: center;

      .email{
        position: relative;

        input{
          border: none;
          border-radius: 40px;
          padding: 20px;
          width: 400px;
          height: 70px;
        }

        .send{
          position: absolute;
          bottom: 0;
          right: 0;
          border-radius: 50%;
          padding: 26px;
          cursor: pointer;
          background-color: $bg-yellow;

          i{
            color: $bg-white;
          }
        }
      }
    }
  }
</style>