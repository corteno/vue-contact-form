<template>
    <form @submit.prevent="onSubmit" class="contact-form-wrapper">
        <FormInput type="text" id="" name="contact-name" label="Test"
                   v-model="contactName" />
        <FormInput type="email" label="E-mail" />
        <FormInput textarea label="Message"/>
        <input type="submit" class="contact-form-submit" value="Send">
        <!--<div class="contact-form-input-wrapper">
            <input type="text" class="contact-form-input" name="contact-name" id="contact-name" required>
            <label for="contact-name">Name</label>
        </div>
        <div class="contact-form-input-wrapper">
            <input type="email" class="contact-form-input" name="contact-email" id="contact-email" required>
            <label for="contact-email">Email</label>
        </div>
        <div class="contact-form-input-wrapper">
            <textarea class="contact-form-input" name="contact-message" id="contact-message" required></textarea>
            <label for="contact-message">Message</label>
        </div>
        <div class="contact-form-input-wrapper">

        </div>-->
    </form>
</template>

<script>
    import FormInput from "./FormInput";

    export default {
        name: "ContactForm",
        components: {FormInput},
        data: function(){
            return {
                contactName: ''
            }
        },
        methods: {
            onSubmit: () => {

            }
        }

    }
</script>

<style>
    .contact-form-wrapper{
        display: flex;
        flex-direction: column;
        max-width: 400px;
        justify-self: center;
        margin: 0 auto;
    }

    .contact-form-submit {
        font-family: NunitoBold, sans-serif;
        text-transform: uppercase;
        background: transparent;
        border: 1px solid #7f7f7f;
        padding: 10px 20px;
        color: #7f7f7f;
        border-radius: 4px;
        cursor: pointer;

        transition: 0.2s all;
    }

    .contact-form-submit:hover{
        color: #313131;
        border-color: #313131;
    }


</style>