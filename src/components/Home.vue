<template>
   <header class="header">
       <div v-bind:class="menuStyles">
           <!--FOR SMALLER SCREENS-->
            <input type="checkbox" id="navi-box">
            <label for="navi-box" class="button">
                <span class="icon"></span>
            </label>
            <div class="menu-background"></div>
            <!--END-->

           <ul class="navigation__group">
               <li class="navigation__item"><a class="navigation__link" href="#">Home</a></li>
               <li class="navigation__item"><a class="navigation__link" href="#">About</a></li>
               <li class="navigation__item"><a class="navigation__link" href="#">Services</a></li>
               <li class="navigation__item"><a class="navigation__link" href="#">Contact</a></li>
           </ul>
       </div>
       <div class="header__heading-block">
           <h1 class="header__heading">Keep <span class="spin"></span></h1>
           <p class="header__sub-text">A simple responsive website</p>
       </div>
   </header>
</template>

<script>

import {eventBus} from '../main.js';

export default {

    data() {
        return {
            scrollPosition: 0,
            menuStyles: {
                navigation: true,
                navigation__fixed: false
            }
        }
    },

    created() {
        eventBus.$on('position', (e) => {
            if (e > 20) {
                this.menuStyles.navigation = false;
                this.menuStyles.navigation__fixed = true;
            } else if (e < 20) {
                this.menuStyles.navigation = true;
                this.menuStyles.navigation__fixed = false;
            }
        });

    }

}
</script>

<style lang="scss" scoped>
    .navigation,
    .navigation__fixed {
        position: fixed;
        top: 0;
        right: 0;
        width: 100%;
        text-align: right;
        transition: all .2s;

     &__fixed {
        background-color: #3b3b3b;
        color: #fff;
        z-index: 2;
     }

     input {
         display: none;
     }

     //////////////// SMALLER SCREENS

      @media only screen and (max-width: 900px) {

        & {
            position: unset;
            color: #fff;
        }

        input { display: none;}

        .button {
            display: inline-block;
            position: fixed;
            top: 5px;
            right: 20px;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            //background-color: #ccc;
            text-align: center;
            cursor: pointer;
            z-index: 20;

                .icon,
                .icon::before,
                .icon::after {
                content: '';
                display: inline-block;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                width: 20px;
                height: 2px;
                border-radius: 5px;
                background-color: #111;


            }

            .icon::before,
            .icon::after {
                position: absolute;
                transition: all .2s;
            }

            .icon::before {
                top: 7px;
            }

            .icon::after {
                top: -5px;
            }

            &:hover .icon::before {
                top: 8px;
            }

            &:hover .icon::after {
                top: -6px;
            }
        }

        .menu-background {
            display: inline-block;
            position: fixed;
            top: 15px;
            right: 30px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: transparent;
        }

        &__group {
            list-style: none;
            position: fixed;
            top: 50%;
            left: -50%;
            transform: translate(-50%, -50%);
            font-size: 4rem;
            text-align: center;
        }

        &__item {
            padding: 1.5rem;
            letter-spacing: .5rem;
            text-transform: uppercase;
        }

        &__link {
            position: relative;
            &:link,
            &:visited {
                color: inherit;
                text-decoration: none;
                transition: all .1s;
            }

            &:hover,
            &:active,
            &:focus {
                color: #111;
                padding-bottom: .3rem;
                //border-bottom: 1px solid #53A80D;
            }
        }

        input:checked ~ .menu-background {
            position: fixed;
            transform: scale(100);
            z-index: 10;
        }

        input:checked ~ .navigation__group {
            left: 50%;
            z-index: 30;
        }

        input:checked ~ .menu-background {
            background-color: #E3C100;
        }

        input:checked + .button .icon {
            background-color: transparent;
        }

        input:checked + .button .icon::before {
            transform: rotate(45deg);
            top: 0;
        }

        input:checked + .button .icon::after {
            transform: rotate(-45deg);
            top: 0;
        }




    }

     ///////////////

     @media only screen and (min-width: 900px) {

        &__group {
            list-style: none;
        }

        &__item {
            display: inline-block;
            padding: 1.5rem;
            text-transform: uppercase;
        }

        &__link {
            position: relative;
            &:link,
            &:visited {
                color: inherit;
                text-decoration: none;
                transition: all .1s;
            }

            &:hover,
            &:active,
            &:focus {
                color: #53A80D;
                padding-bottom: .3rem;
                //border-bottom: 1px solid #53A80D;
            }
        }

        }
    }


    .header {
        position: relative;
        height: 90vh;
        background-image: linear-gradient(to right, rgba(#000, .0)), url(../assets/img/home1.jpg);
        background-attachment: fixed; // parallax scrolling
        background-repeat: no-repeat;
        background-size: cover;
        background-position: bottom;


        &__heading-block {
            position: absolute;
            top: 35%;
            left: 50%;
            transform: translate(-50%, -50%);

            border-bottom: 1px solid #ccc;

             @media only screen and (max-width: 900px) {
                 top: 45%;
             }
        }

        &__heading {
            font-size: 5rem;
            font-weight: 300;
            letter-spacing: .5rem;
            line-height: 1.5;
            animation-delay: 1s;
            animation: fadeIn 3s;
            animation-fill-mode: backwards;

            @media only screen and (max-width: 900px) {
                font-size: 5rem;
                text-align: center;
                }

            }

            &__heading .spin {
                @media only screen and (max-width: 900px) {
                    display: block;
                    line-height: 1.5;
                    margin-top: -15px;
                }
            }



        &__heading .spin::after {
            content: '';
            display: inline-block;
            width: 30rem;
            font-size: 5rem;
            text-align: center;
            animation: spin 20s linear infinite;
            animation-delay: 1.2s;

            @media only screen and (max-width: 900px) {
                width: 20rem;
                font-size: 3rem;
                }

            @media only screen and (max-width: 600px) {
                width: 15rem;
                font-size: 2rem;
                line-height: 2;
                }

        }

        &__sub-text {
            padding-top: 3rem;
            padding-bottom: 2rem;
            font-size: 2.4rem;
            font-weight: 300;
            letter-spacing: .5rem;
            text-align: center;
            animation: fadeIn 3s;
            animation-delay: 2.5s;
            animation-fill-mode: backwards;

             @media only screen and (max-width: 900px) {
                font-size: 2rem;
                letter-spacing: .2rem;
                padding-top: 1.5rem;
                }

            @media only screen and (max-width: 900px) {
                font-size: 1.6rem;
                letter-spacing: .1rem;
                padding-top: 1.5rem;
                }
        }
    }


    //ANIMATIONS
    @keyframes fadeIn {
        from {opacity: 0;}
        to {opacity: 1;}
    }

    @keyframes spin {
        0% {content: 'improving'; background-color: #FA8B00; color: #fff}
        25% {content: 'curious'; background-color: #F92500; color: #fff}
        50% {content: 'learning'; background-color: #50A707; color: #fff}
        75% {content: 'growing'; background-color:#CD4E75; color: #fff}
        100% {content: 'moving'; background-color:#EACF00; color: #fff}






    }
</style>
