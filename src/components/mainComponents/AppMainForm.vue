<script>
export default {
    name: 'AppMainForm',
    data() {
        return {
        }
    },
}

</script>

<template>
    <section>
        <div class="container">
            <div class="container child">
                <div class="contactUs">
                    <div class="map">
                    </div>
                    <div class="formBox">
                        <h2>Contanct Us<span>.</span></h2>
                        <p>Keep in touch with us and discover our servicies</p>
                        <div class="line"></div>
                        <div class="form">
                            <form>
                                <div class="userData">
                                    <div>
                                        <label for="name"></label>
                                        <input type="text" id="name" name="name" placeholder=" Your name" required>
                                    </div>
                                    <div>
                                        <label for="email"></label>
                                        <input type="email" id="email" name="email" placeholder=" Your email" required>
                                    </div>
                                </div>
                                <div class="userMessage">
                                    <label for="message"></label>
                                    <input type="text" id="message" name="message" placeholder=" Write a Message..."
                                        required>
                                </div>
                                <div class="submit">
                                    <button class="send-btn">SEND<i class="fa-solid fa-arrow-right-long"></i></button>
                                </div>
                            </form>


                        </div>
                    </div>
                </div>
                <div class="partners">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

.container {
    @include mixins.container-margin;
}

.child {
    padding-top: 96px;
}

.contactUs {
    @include mixins.d-flex-between;
    height: 300px;
    gap: 48px;

    .map {
        background-image: url(../../assets/img/h1-contact-rev-01.png);
        width: 50%;
        height: 80%;
        background-size: contain;
        background-repeat: no-repeat;
    }

    .formBox {
        width: 50%;
        height: 100%;

        .line {
            margin: 8px 0;
            width: 80px;
            height: 1.5px;
            background-color: $orange-first-color;
        }

        h2 {
            font-size: 42px;
        }

        p {
            color: $gray-second-color;
            margin-bottom: 12px;
        }

        span {
            color: $orange-first-color;
        }
    }
}

form {
    margin-top: 24px;

    label,
    input {
        border: none;
        border-bottom: 1px solid lightgray;
    }

    .userData {
        @include mixins.d-flex-between;
        gap: 12px;

        div {
            width: 50%;
            margin-bottom: 24px;

        }

        input {
            width: 100%;
        }

    }

    .userMessage {
        margin: 24px 0;

        input {
            padding-bottom: 48px;
            width: 100%;
        }
    }

    .submit {
        .send-btn {
            @include mixins.button-orange;
            background-color: $orange-first-color;
        }
    }

}
</style>