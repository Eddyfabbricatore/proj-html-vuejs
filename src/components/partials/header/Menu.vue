<script>
  import headerMenu from '../../../data/headerMenu';

  export default {
    name: 'Menu',

    data(){
      return{
        headerMenu
      }
    },

    props:{
      buttonText: String
    }
  }
</script>

<template>
  <div class="menu">
    <nav>
      <ul>
        <li v-for="(item, index) in headerMenu" :key="index">
          <a href="#">{{ item.text }} <i :class="item.icon"></i></a>
        </li>
      </ul>
    </nav>

    <button class="btn btn-yellow">{{ buttonText }}</button>
  </div>
</template>

<style lang="scss" scoped>
  .menu{
    display: flex;
    align-items: center;

    ul{
      display: flex;

      li{
        margin-right: 40px;

        a{
          color: #fff;
          display: flex;

          i{
            margin-left: 10px;
            font-size: .8rem;
          }

          &:hover{
            color: #e9d758
          }
        }
      }
    }
  }
</style>