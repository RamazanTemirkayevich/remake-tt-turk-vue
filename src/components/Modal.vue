<template>
    <div class="modal">
        <div class="modal-box">
            <slot />
        </div>
    </div>
</template>

<style lang="scss">
    @media (min-width: 320px) {
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 99;
            background-color: rgba(0, 0, 0, 0.2);
            
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 35px 10px;

            &-box {
                width: 100%;
                height: 100%;
                padding: 15px;
                display: flex;
                align-items: center;
                justify-content: center;
                background: #FFFFFF;
                border-radius: 10px;

                &__container {
                    width: 100%;
                    height: 100%;

                    &>form {
                        display: flex;
                        flex-direction: column;
                        justify-content: space-between;
                        width: 100%;
                        height: 100%;

                        .modal-box__container--title {
                            display: flex;
                            width: 100%;
                            justify-content: space-between;

                            .modal-name {
                                font-weight: 500;
                                font-size: 20px;
                                line-height: 23px;
                                color: #0A0A0A;
                            }

                            .modal-close {
                                border: none;
                                background: none;
                                cursor: pointer;
                                outline: none;
                            }
                        }

                        .modal-box__container--raiting {
                            display: flex;
                            flex-direction: column;

                            .raiting-title {
                                font-weight: 500;
                                font-size: 16px;
                                line-height: 19px;
                                color: #404040;                           
                            }

                            .raiting-stars {
                                margin-top: 7px;
                                width: 135px;
                                display: flex;
                                justify-content: space-between;

                                &>img {
                                    width: 22.22px;
                                }
                            }
                        }

                        .advantages-form, .disadvantages-form, .comment-form, .upload-images {
                            display: flex;
                            flex-direction: column;

                            &__title {
                                font-weight: 500;
                                font-size: 16px;
                                line-height: 19px;
                                color: #404040;
                            }

                            &>input {
                                margin-top: 7px;
                                width: 100%;
                                height: 45px;
                                text-indent: 15px;
                                background: #FFFFFF;
                                border: 2px solid #EEEEEE;
                                border-radius: 7px;
                                outline: none;
                                gap: 10;
                            }

                            &>input:hover {
                                border: 2px solid $main-color;
                            }

                            .comment-form__input {
                                margin-top: 7px;
                                width: 100%;
                                height: 135px;
                                text-indent: 15px;
                                padding-top: 15px;
                                background: #FFFFFF;
                                border: 2px solid #EEEEEE;
                                border-radius: 7px;
                                outline: none;
                            }

                            .comment-form__input:hover {
                                border: 2px solid $main-color;
                            }

                            &__btn {
                                margin-top: 7px;
                                display: flex;
                                align-items: center;
                                justify-content: center;
                                width: 100%;
                                height: 50px;
                                background: #FAFAFA;
                                border-radius: 6.25px;
                                border: none;
                            }
                        }

                        .modal-btn {
                            display: flex;
                            flex-direction: row;
                            justify-content: center;
                            align-items: center;
                            width: 100%;
                            height: 40px;
                            background: $main-color;
                            border-radius: 5px;

                            font-weight: 500;
                            font-size: 18px;
                            line-height: 21px;
                            color: #FFFFFF;
                        }
                    }
                }
            }

            @media (min-width: 1024px) {
                &-box {
                    width: 620px;
                    height: 700px;
                    padding: 30px;
                }
            }
        }
    }
</style>