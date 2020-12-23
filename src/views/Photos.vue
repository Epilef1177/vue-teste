<template>
    <div class="body">
        <section>
            <img src="../assets/photos/blackbird.jpg" alt="">
        </section>
        <section>
            <img src="../assets/photos/dolphin.jpg" alt="">
        </section>
        <section>
            <img src="../assets/photos/fallow-deer.jpg" alt="">
        </section>
        <section>
            <img src="../assets/photos/kingfisher.jpg" alt="">
        </section>
        <section >
            <img src="../assets/photos/owl.jpg" id="owl" alt="">
        </section>
        <section>
            <img src="../assets/photos/turtle.jpg" id="turtle" alt="">
        </section>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .body {
        min-height: 500px;
    }
    img {
        margin: 30px;
        height: 200px;
        transition: all 1s ease-in-out;
    }
    img:hover {
        transform: scale(1.5);

    }
    /*#owl {
        height: 227px;
    }
    #turtle {
        height: 190px;
    }
    div {
        display: inline-block;
    }*/
    section {
        display: inline-block;
    }
</style>