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
        <div class="row">
            <div class="col-3">
                <div class="card">
                    <div class="card__header">
                        <img class="card__img" src="../assets/img/services-4.jpeg" alt="" />
                    </div>
                    <div class="card__content">
                        <h3 class="card__heading">Column One</h3>
                        <p class="card__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illo, ducimus dicta. Quisquam rerum in, unde quidem quasi, distinctio aliquam recusandae dolorum dolorem ut at quaerat nulla autem aliquid, quia repellendus.</p>
                        <a href="#" class="btn btn--basic margin-t-m">Read it</a>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div class="card">
                    <div class="card__header">
                        <img class="card__img" src="../assets/img/services-5.jpeg" alt="" />
                    </div>
                    <div class="card__content">
                        <h3 class="card__heading">Column One</h3>
                        <p class="card__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illo, ducimus dicta. Quisquam rerum in, unde quidem quasi, distinctio aliquam recusandae dolorum dolorem ut at quaerat nulla autem aliquid, quia repellendus.</p>
                        <a href="#" class="btn btn--basic margin-t-m">Read it</a>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div class="card">
                    <div class="card__header">
                        <img class="card__img" src="../assets/img/services-6.jpeg" alt="" />
                    </div>
                    <div class="card__content">
                        <h3 class="card__heading">Column One</h3>
                        <p class="card__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illo, ducimus dicta. Quisquam rerum in, unde quidem quasi, distinctio aliquam recusandae dolorum dolorem ut at quaerat nulla autem aliquid, quia repellendus.</p>
                        <a href="#" class="btn btn--basic margin-t-m">Read it</a>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div class="card">
                    <div class="card__header">
                        <img class="card__img" src="../assets/img/services-7.jpeg" alt="" />
                    </div>
                    <div class="card__content">
                        <h3 class="card__heading">Column One</h3>
                        <p class="card__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illo, ducimus dicta. Quisquam rerum in, unde quidem quasi, distinctio aliquam recusandae dolorum dolorem ut at quaerat nulla autem aliquid, quia repellendus.</p>
                        <a href="#" class="btn btn--basic margin-t-m">Read it</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <div class="card">
                    <div class="card__header card__header--big">
                        <img class="card__img card__img--big" src="../assets/img/services-7.jpeg" alt="" />
                    </div>
                    <div class="card__content">
                        <h3 class="card__heading">One Big Column</h3>
                        <p class="card__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illo, ducimus dicta. Quisquam rerum in, unde quidem quasi, distinctio aliquam recusandae dolorum dolorem ut at quaerat nulla autem aliquid, quia repellendus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere accusamus nam excepturi eligendi dolores quibusdam cupiditate voluptatum quisquam natus modi. Inventore debitis saepe assumenda corrupti quisquam doloremque eius ad aspernatur! Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae illo modi distinctio explicabo dolorem, provident deleniti repudiandae recusandae cumque vero, culpa quas dolorum, necessitatibus accusamus. Maxime cupiditate maiores quae illum!

                        </p>
                        <a href="#" class="btn btn--basic margin-t-m">Read more</a>
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

        &__photo {
            width: 100%;
            max-width: 100%;
            height: auto;
        }
    }

    .section-header {
        position: relative;
        height: 25vh;
        background-image: url(../assets/img/services-2.jpeg);
        background-size: cover;
        background-attachment: fixed;
        // background-position-y: -7rem;
        // background-position-x: -20rem;
        //background-position: 0 - 7rem;
        background-repeat: no-repeat;

        @media(max-width: 600px) {
            background-image: url(../assets/img/services-2.jpeg);
            background-position: center;
        }

    }

</style>
