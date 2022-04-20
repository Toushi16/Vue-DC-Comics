<template>
  <header class="main-header">

      <div class="container">

          <figure class="logo">
              <img src="../assets/img/dc-logo.png" alt="">
          </figure>

          <nav class="main-nav">
              <ul>
                  <li v-for="(link,i) in links" :key="i" class="nav-item" :class="link.active ? 'active' : '' "> 
                      <a href="#">{{link.text}}</a>
                  </li>
              </ul>

          </nav>
      </div>

  </header>
</template>

<script>
export default {
    data() {
        return {
            links: [
                {
                    text:'CHARACTERS',
                    href:'#'
                },
                {
                    text:'COMICS',
                    href:'#',
                    active: true
                },
                {
                    text:'MOVIES',
                    href:'#'
                },
                {
                    text:'TV',
                    href:'#'
                },
                {
                    text:'GAMES',
                    href:'#'
                },
                {
                    text:'COLLECTIBLES',
                    href:'#'
                },
                {
                    text:'VIDEOS',
                    href:'#'
                },
                {
                    text:'FANS',
                    href:'#'
                },
                {
                    text:'NEWS',
                    href:'#'
                },
                {
                    text:'SHOP',
                    href:'#'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';      

.main-header {
    // min-height: 118px;

    .container {
        display: flex;
        justify-content: space-between;
        min-height: 118px;

        .logo {
            align-self: center;

            img {
                display: block;
            }
        }
    }

    .main-nav {
        display: flex;
        gap: 30px;
        font-size: 15px;

        ul {
            display: contents;
        }

        .nav-item {
            font-weight: 700;

            &:hover {
                color: $blue;
            }

            
            a {
                display: flex;
                align-items: center;
                position: relative;
                height: 100%;
            }

            &.active, &:hover {

                a:after {
                    content: '';
                    display: block;
                    height: 4px;
                    position: absolute;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background-color: $blue;
                }
            }
        }
    }
}

</style>