<script>
/* import AppThumbs from "./AppLocandine.vue"; */
export default {
    name: "AppContent",
    components: {
        AppThumbs
    },
    data() {
        return {
            Tumbs: [
                {
                    thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
                    price: '$19.99',
                    series: 'Action Comics',
                    type: 'comic book',
                },
                {
                    thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
                    price: '$3.99',
                    series: 'American Vampire 1976',
                    type: 'comic book',
                },
                {
                    thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
                    price: '$16.99',
                    series: 'Aquaman',
                    type: 'graphic novel',
                },
                {
                    thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
                    price: '$2.99',
                    series: 'Batgirl',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
                    price: '$3.99',
                    series: 'Batman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
                    price: '$2.99',
                    series: 'Batman Beyond',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
                    price: '$3.99',
                    series: 'Batman/Superman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
                    price: '$4.99',
                    series: 'Batman/Superman Annual',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
                    price: '$5.99',
                    series: 'Batman: The Joker War Zone',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
                    price: '$6.99',
                    series: 'Batman: Three Jokers',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
                    price: '$4.99',
                    series: 'Batman: White Knight Presents: Harley Quinn',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
                    price: '$16.99',
                    series: 'Catwoman',
                    type: 'graphic novel',
                },
            ]
        }
    }
} 
</script>

<template>
    <div class="wrapper-content">
        <section class="jumbotron">
            <img src="../assets/jumbotron.jpg" alt="">
        </section>
        <section class="locandine">
            <h3 class="title">CURRENT SERIES</h3>
            <AppLocandine v-for="(element, index) in Thumbs" :key="index" :immagine="element.thumb"
                :prezzo="element.price" :tipo="element.series" />
            <button>LOAD MORE</button>
        </section>
    </div>
</template>


<style scoped lang="scss">
@use "../style/mixins" as *;
@use "../style/variables" as *;
.wrapper-content {
    // height: 500px;
    width: 100%;
    background-color: $mainblack;
    color: white;
    .jumbotron {
        img {
            width: 100%;
            max-height: 400px;
            object-fit: cover;
            object-position: 0 0;
        }
    }
    .locandine {
        position: relative;
        @include ms_container (700px, 0 auto);
        @include flex(row, center, stretch);
        flex-wrap: wrap;
        padding: 30px 0;
        .title {
            color: white;
            background-color: $mainblu;
            padding: 10px 15px;
            position: absolute;
            border-radius: 20px;
            border: none;
            top: -22px;
            left: 0;
        }
        button {
            background-color:$mainblu;
            color: white;
            margin-top: 30px;
            padding: 10px 30px;
            border-radius: 20px;
            border: none;
            font-size: 16px;
            cursor: pointer;
        }
    }
}
</style>