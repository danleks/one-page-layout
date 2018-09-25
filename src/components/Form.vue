<template>
    <section class="section-form">
        <div class="row">
            <div class="col-12">
                <div class="contact">
                    <div class="contact__background">&nbsp;</div>

                    <div class="contact__form vertically-centered">
                        <h3 class="contact__heading">Contact Form</h3>
                        <div class="row margin-t-b">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur porro numquam neque harum! Hic molestiae eligendi laborum quos sit recusandae.</p>
                        </div>
                        <div class="row">
                            <div class="col-6">
                                <div class="form-group">
                                    <input placeholder="Name" class="form-group__item" type="text">
                                    <input placeholder="Email" class="form-group__item" type="email">
                                    <input placeholder="Subject" class="form-group__item" type="text">
                                </div>
                            </div>
                            <div class="col-6">
                                <div class="form-group">
                                    <textarea placeholder="Your message" class="form-group__item" name="text"></textarea>
                                </div>
                            </div>
                        </div>
                    </div>
            </div>
        </div>

        </div>
</section>
</template>

<style lang="scss" scoped>

    .contact {
        position: relative;

        &__heading {
            font-size: 3rem;
            text-align: center;
        }

        &__background {
            background-image: url(../assets/img/contact.jpg);
            height: 70vh;
            filter: blur(.5rem);
        }

        &__form {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 50%;
            margin: 0 auto;

            & p {
                padding: 4rem;
                border-radius: .6rem;
                font-size: 1.5rem;
                letter-spacing: .1rem;
                text-align: center;
                background-color: rgba(#000, .2);
            }
        }

        .form-group {

            &__item {
                width: 100%;
                padding: .8rem;
                border: none;
                border-radius: .6rem;
                background-color: rgba(#000, .2);

                &::placeholder {
                    color: #000;
                }


                &:not(:last-child) {
                    margin-bottom: 1.7rem;
                }
            }

            textarea {
                height: 13rem;
            }
        }
    }

</style>
