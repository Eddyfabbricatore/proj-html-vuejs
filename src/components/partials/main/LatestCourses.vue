<script>
  export default {
    name: 'LatestCourses'
  }
</script>

<template>
  <section class="latest-courses">
    <div class="container">
      <h2>Latest Courses</h2>

      <div class="row">
        <div class="col">
          <div class="card">
            <div class="image">
              <img src="../../../assets/img/Decisions-icon.png" alt="">
            </div>

            <h5>Make Better Decisions</h5>

            <p><i class="fa-regular fa-user"></i>Teacher: <span>James Collins</span></p>

            <p><i class="fa-regular fa-money-bill-1"></i>Price: <span>$21.00</span></p>
          </div>
        </div>

        <div class="col">
          <div class="card">
            <div class="image">
              <img src="../../../assets/img/Speaker-icon.png" alt="">
            </div>

            <h5>How to be a speakers</h5>

            <p><i class="fa-regular fa-user"></i>Teacher: <span>James Collins</span></p>

            <p><i class="fa-regular fa-money-bill-1"></i>Price: <span>Free</span></p>
          </div>
        </div>

        <div class="col">
          <div class="card">
            <div class="image">
              <img src="../../../assets/img/Network-icon.png" alt="">
            </div>

            <h5>Network Introductions</h5>

            <p><i class="fa-regular fa-user"></i>Teacher: <span>James Collins</span></p>

            <p><i class="fa-regular fa-money-bill-1"></i>Price: <span>Free</span></p>
          </div>
        </div>

        <div class="col">
          <div class="card">
            <div class="image">
              <img src="../../../assets/img/Brand-icon.png" alt="">
            </div>

            <h5>Brand management</h5>

            <p><i class="fa-regular fa-user"></i>Teacher: <span>James Collins</span></p>

            <p><i class="fa-regular fa-money-bill-1"></i>Price: <span>Free</span></p>
          </div>
        </div>
      </div>

      <div class="content">
        <div class="text">
          <div class="image">
            <img src="../../../assets/img/Exam-icon.png" alt="">
          </div>

          <h2>The most efficient examination method</h2>

          <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teachers from our university has an influence on how students are evaluated at his/her subject.</p>

          <button class="btn btn-red">Discover the Method</button>
        </div>

        <div class="img">
          <img src="../../../assets/img/Exam-Illustration.png" alt="">
        </div>
      </div>

      <div class="second-content">
        <div class="img">
          <img src="../../../assets/img/Girl-Illustration.png" alt="">
        </div>

        <div class="text">
          <div class="image">
            <img src="../../../assets/img/Exam-icon-1.png" alt="">
          </div>

          <h2>The most efficient examination method</h2>

          <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teachers from our university has an influence on how students are evaluated at his/her subject.</p>

          <button class="btn btn-red">List of Fees</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  h2{
    margin-top: 50px;
  }

  .row{
    display: flex;
    margin-top: 50px;
    margin-bottom: 60px;
    width: 100%;

    .col{
      padding: 20px;
      width: calc(100% / 4);

      .card{
        display: flex;
        flex-direction: column;
        align-items: center;
        border-radius: 5px;
        padding: 20px;
        box-shadow: 1px 1px 5px 10px #f7f8fa;

        .image{
          margin-bottom: 20px;
          width: 50px;
          height: 50px;
        }

        h5,
        p{
          margin-bottom: 15px;
        }

        h5{
          font-size: 1.1rem;
          color: #223441
        }

        p{
          color: #8b8b8a;
        }

        i{
          margin-right: 5px;
        }

        span{
          color: #5c5e6c;
        }
      }
    }
  }

  .content,
  .second-content{
    display: flex;
    width: 100%;
  }

  .content{
    .text,
    .img{
      width: 50%;
    }

    .text{
      .image{
        width: 70px;
        height: 70px;
      }

      h2,
      p{
        margin-bottom: 40px;
      }

      h2{
        margin-top: 20px;
      }

      p{
        font-size: 1.1rem;
        color: #434959;
      }
    }
    
    .img{
      padding: 50px;
    }
  }

  .second-content{
    .text,
    .img{
      width: 50%;
    }

    .img{
      padding: 50px;
    }

    .text{
      .image{
        width: 70px;
        height: 70px;
      }

      h2{
        margin-top: 20px;
      }

      h2,
      p{
        margin-bottom: 40px;
      }

      p{
        color: #434959;
      }
    }
  }
</style>