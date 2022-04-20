<template>
  <footer class="footer">
      <section class="footer__body">

          <div class="container">

              <div class="col">

                  <div class="widget">
                      <h4 class="widget__title">DC COMICS</h4>
                      <ul class="widget__menu">
                          <li>Characters</li>
                          <li>Comics</li>
                          <li>Movies</li>
                          <li>TV</li>
                          <li>Games</li>
                          <li>Videos</li>
                          <li>News</li>
                      </ul>
                  </div>

                  <div class="widget">
                      <h4 class="widget__title">SHOP</h4>
                      <ul class="widget__menu">
                          <li>Shop DC</li>
                          <li>Shop DC Collectibles</li>
                      </ul>
                  </div>

              </div>

              <div class="col">

                  <div class="widget">
                      <h4 class="widget__title">DC</h4>
                      <ul class="widget__menu">
                          <li>Terms Of Use</li>
                          <li>Privacy policy (New)</li>
                          <li>Ad Choices</li>
                          <li>Advertising</li>
                          <li>Jobs</li>
                          <li>Subscriptions</li>
                          <li>Talent Workshops</li>
                          <li>CPSC Certificates</li>
                          <li>Ratings</li>
                          <li>Shop Help</li>
                          <li>Contact Us</li>
                      </ul>
                  </div>
                  
              </div>

              <div class="col">

                  <div class="widget">
                      <h4 class="widget__title">SITES</h4>
                      <ul class="widget__menu">
                          <li>DC</li>
                          <li>MAD Magazine</li>
                          <li>DC Kids</li>
                          <li>DC Universe</li>
                          <li>DC Power Visa</li>
                      </ul>
                  </div>
                  
              </div>

          </div>
          
      </section>

      <section class="footer__social-bar">
        <div class="container">   
            <button class="sign-in">SIGN-UP NOW!</button>

            <div class="follow-us">
                <span>FOLLOW US</span>
                <ul>
                    <li>
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/img/footer-twitter.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/img/footer-youtube.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/img/footer-pinterest.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/img/footer-periscope.png" alt="">
                    </li>
                </ul>
            </div>

          </div>
          
      </section>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/mixins.scss';

.footer {

    color: white;

    .footer__body {
        background-image:url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-position:center;
        background-size: cover;

        .container {
            padding: 40px 0;
            display: flex;
            background: url('../assets/img/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position: right center;

            .col {

                width: calc( 100% / 9 );

                .widget {
                    @include widget;

                    li {
                        font-size: 14px;
                        color: #959595;
                        cursor: pointer;
                    }
                }
            }
        }
    }

    .footer__social-bar {
        background-color: #303030;
        padding: 25px 0;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .sign-in {
                border: 2px solid $blue;
                font-weight: 700;
                padding: 10px;
                background-color: transparent;
                color: white;
                font-size: 18px;
                cursor: pointer;
            }

            .follow-us {
                display: flex;
                gap: 15px;
                align-items: center;

                img {
                    cursor: pointer;
                }

            span {
                color: $blue;
                font-size: 18px;
                font-weight: 700;
            }

                ul {
                    display: contents;
                }
            }
        }

    }

}

</style>