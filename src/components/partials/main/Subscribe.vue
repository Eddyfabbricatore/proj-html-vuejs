<script>
  export default {
    name: 'Subscribe'
  }
</script>

<template>
  <section class="subscribe">
    <div class="container">
      <h3>Subscribe Now To Our Newsletter</h3>

      <div class="email">
        <input type="email" placeholder="Email address...">

        <div class="send">
          <i class="fa-solid fa-paper-plane"></i>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .subscribe{
    background-color: $bg-red;
    padding: 50px 0;

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
          background-color: $bg-yellow;

          i{
            color: $bg-white;
          }
        }
      }
    }
  }
</style>