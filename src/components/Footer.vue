<script>
  import eduPrime from '../data/footer/eduPrime';
  import network from '../data/footer/network';
  import categories from '../data/footer/categories';
  import themes from '../data/footer/themes';

  export default {
    name: 'Footer',

    data(){
      return{
        eduPrime,
        network,
        categories,
        themes,
        imgSrc: 'src/assets/img/theme_eduprime_logo.png',
        paragraph: 'EduPrime is the most versatile WorldPress theme for educational purposes, showcasing universities, courses, secondary scholl etc.',
        icons: ['fa-brands fa-facebook-f', 'fa-brands fa-twitter', 'fa-brands fa-instagram'],
        firstTitle: 'Get EduPrime',
        secondTitle: 'Networking',
        searchText: 'Search...',
        searchIcon: 'fa-solid fa-magnifying-glass',
        thirdTitle: 'Search Categories',
        rights: 'ModelTheme. All rights reserved',
        back: 'src/assets/img/back-to-top-arrow.svg'
      }
    }
  }
</script>

<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="logo">
            <img :src="imgSrc" alt="Logo EduPrime">
          </div>

          <p>{{ paragraph }}</p>

          <div class="social">
            <i :class="icon" v-for="(icon, index) in icons" :key="index"></i>
          </div>
        </div>

        <div class="col">
          <h5>{{ firstTitle }}</h5>
          
          <nav>
            <ul>
              <li v-for="(textEdu, index) in eduPrime" :key="index">
                <a href="#">{{ textEdu.text }}</a>
              </li>
            </ul>
          </nav>
        </div>

        <div class="col">
          <h5>{{ secondTitle }}</h5>

          <nav>
            <ul>
              <li v-for="(textNet, index) in network" :key="index">
                <a href="#">{{ textNet.text }}</a>
              </li>
            </ul>
          </nav>
        </div>

        <div class="col">
          <div class="search">
            <input type="email" :placeholder="searchText">

            <div class="send">
              <i :class="searchIcon"></i>
            </div>
          </div>

          <h5>{{ thirdTitle }}</h5>

          <div class="category">
            <nav>
              <ul>
                <li v-for="(category, index) in categories" :key="index">
                  <a href="#">{{ category.text }}</a>
                </li>
              </ul>
            </nav>
          </div>

          <p>{{ rights }}</p>
        </div>
      </div>
    </div>

    <div class="theme">
      <div :class="theme.class" v-for="(theme, index) in themes" :key="index">
        <div class="img">
          <img :src="theme.imgSrc" :alt="theme.name">
        </div>

        <span>{{ theme.name }}</span>
      </div>
    </div>

    <div class="back">
      <a href="#start">
        <img :src="back" alt="Start">
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
              cursor: pointer;
              color: $bg-white;
            }
          }

          p,
          li{
            color: #ffffffcc;
          }

          li{
            margin-bottom: 20px;
          }

          .search{
            position: relative;
            cursor: pointer;

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
              ul{
                display: flex;
                justify-content: end;
                flex-wrap: wrap;

                li{
                  border: 1px solid #ffffffcc;
                  border-radius: 20px;
                  margin-left: 8px;
                  padding: 10px 5px;
                  font-size: .8rem;
                }
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
        cursor: pointer;
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