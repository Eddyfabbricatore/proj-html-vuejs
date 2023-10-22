<script>
  export default {
    name: 'Footer'
  }
</script>

<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="logo">
            <img src="../assets/img/theme_eduprime_logo.png" alt="">
          </div>

          <p>EduPrime is the most versatile WorldPress theme for educational purposes, showcasing universities, courses, secondary scholl etc.</p>

          <div class="social">
            <i class="fa-brands fa-facebook-f"></i>

            <i class="fa-brands fa-twitter"></i>

            <i class="fa-brands fa-instagram"></i>
          </div>
        </div>

        <div class="col">
          <h5>Get EduPrime</h5>

          <span>Request a web site</span>

          <span>Browse Themes</span>

          <span>Payment options</span>

          <span>Support System</span>

          <span>Checkout</span>

          <span>Purchase Theme</span>
        </div>

        <div class="col">
          <h5>Networking</h5>

          <span>Purchase Theme</span>

          <span>Our Benefits</span>

          <span>Our Team</span>

          <span>Our Services</span>

          <span>Others Products</span>

          <span>My account</span>
        </div>

        <div class="col">
          <div class="search">
            <input type="email" placeholder="Search...">

            <div class="send"><i class="fa-solid fa-magnifying-glass"></i></div>
          </div>

          <h5>Search Categories</h5>

          <div class="category">
            <span>Economy</span>

            <span>Design</span>

            <span>Coaching</span>

            <span>Business</span>

            <span>Medicine</span>

            <span>Law</span>

            <span>Fitness</span>
          </div>

          <p>ModelTheme. All rights reserved</p>
        </div>
      </div>
    </div>

    <div class="theme">
      <div class="purchase">
        <div class="img">
          <img src="../assets/svg/svg-3.svg" alt="">
        </div>

        <span>Purchase Theme</span>
      </div>

      <div class="related">
        <div class="img">
          <img src="../assets/svg/svg-2.svg" alt="">
        </div>

        <span>Related Theme</span>
      </div>
    </div>

    <div class="back">
      <a href="#top">
        <img src="../assets/img/back-to-top-arrow.svg" alt="">
      </a>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  @use '../scss/variables.scss' as *;
  
  footer{
    position: relative;
    padding: 100px 0;
    background-color: $bg-red;

    .container{
      padding: 0 80px;

      .row{
        display: flex;
        width: 100%;

        .col{
          display: flex;
          flex-direction: column;
          align-items: center;
          width: calc(100% / 4);

          h5{
            margin-bottom: 30px;
            font-size: 1.1rem;
            color: $bg-white;
          }

          .logo{
            margin-bottom: 30px;
            width: 220px;
            height: 50px;
          }

          .social{
            margin-top: 30px;

            i{
              border: 1px solid #e9d758;
              border-radius: 50%;
              margin-right: 15px;
              padding: 20px;
              color: $bg-white;
            }
          }

          p,
          span{
            color: #ffffffcc;
          }

          span{
            margin-bottom: 20px;
          }

          .search{
            position: relative;

            input{
              border: none;
              border-radius: 40px;
              margin-bottom: 30px;
              padding: 20px;
              width: 300px;
            }

            .send{
              position: absolute;
              bottom: 30px;
              right: 0;
              border-radius: 50%;
              padding: 19px;
              color: $bg-white;
              background-color: $bg-yellow;
            }
          }

          &:last-of-type{
            align-items: end;

            .category{
              display: flex;
              justify-content: end;
              flex-wrap: wrap;

              span{
                border: 1px solid #ffffffcc;
                border-radius: 20px;
                margin-left: 5px;
                padding: 10px;
                font-size: .8rem;
              }
            }

            p{
              color: $bg-yellow;
            }
          }
        }
      }
    }

    .theme{
      position: absolute;
      bottom: 30px;
      left: 30px;
      width: 180px;

      .purchase,
      .related{
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 5px;
        width: 100%;
        height: 40px;
        color: $color-theme;
        background-color: $bg-theme;

        .img{
          margin-right: 5px;
          width: 20px;
          height: 20px;
        }
      }

      .purchase{
        margin-bottom: 15px;
      }
    }

    .back{
      position: absolute;
      bottom: 30px;
      right: 30px;
      border-radius: 50%;
      padding: 15px;
      width: 50px;
      height: 50px;
      cursor: pointer;
      background-color: $bg-yellow;
    }
  }
</style>