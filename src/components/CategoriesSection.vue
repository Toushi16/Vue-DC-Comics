<template>
    <section id="categories">
        <div class="container">
            <ul class="cat-wrapper">
              <li v-for="(el,i) in categories" :key="i" class="cat-item">
                  <img :src="el.src" alt="">
                  {{el.text}}
              </li>
          </ul>
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                categories: [
                    {
                        text:'DIGITAL COMICS',
                        src:require('../assets/img/buy-comics-digital-comics.png')
                    },
                    {
                        text:'DC MERCHANDISE',
                        src:require('../assets/img/buy-comics-merchandise.png')
                    },
                    {
                        text:'SUBSCRIPTION',
                        src:require('../assets/img/buy-comics-subscriptions.png')
                    },
                    {
                        text:'COMIC SHOP LOCATOR',
                        src:require('../assets/img/buy-comics-shop-locator.png')
                    },
                    {
                        text:'DC POWER VISA',
                        src:require('../assets/img/buy-dc-power-visa.svg')
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

#categories {
    background-color: $blue;
    color: white;

    .cat-wrapper {
        display: flex;
        align-items: center;
        padding: 50px 0;
    }

    .cat-item {
        flex-basis: 0;
        flex-grow: 1;
        text-align: center;
        display: flex;
        gap: 15px;
        align-items: center;
        cursor: pointer;

        img {
            height: 60px;
        }
    }
}

</style>