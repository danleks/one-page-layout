<template>
    <section class="section-services">
        <div class="row">
            <div class="col-12">
                <div class="section-header">
                    <div class="vertically-centered">
                        <h2 class="heading-secondary">Our Services</h2>
                    <p class="section-header__text margin-t-s">Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .section-services {
        margin-top: 3rem;
    }

    .section-header {
        position: relative;
        height: 25vh;
        background-image: linear-gradient(to right, rgba(#f6f6f6, .4)) ,url(../assets/img/home.jpg);
        background-size: cover;
        background-attachment: fixed;
        // background-position-y: -7rem;
        // background-position-x: -20rem;
        background-position: center;
        background-repeat: no-repeat;

    }

</style>
