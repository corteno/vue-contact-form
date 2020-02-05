<template>
    <form class="contact-form-wrapper">
        <div class="contact-form-input-wrapper">
            <input type="text" class="contact-form-input" name="contact-name" id="contact-name" required>
            <label for="contact-name">Name</label>
        </div>
        <div class="contact-form-input-wrapper">
            <input type="email" class="contact-form-input" name="contact-email" id="contact-email" required>
            <label for="contact-email">Email</label>
        </div>
        <div class="contact-form-input-wrapper">
            <textarea type="text" class="contact-form-input" name="contact-message" id="contact-message" required></textarea>
            <label for="contact-message">Message</label>
        </div>
        <div class="contact-form-input-wrapper">
            <input type="submit" class="contact-form-submit" value="Send">
        </div>
    </form>
</template>

<script>
    export default {
        name: "ContactForm"
    }
</script>

<style scoped>
    .contact-form-wrapper{
        display: flex;
        flex-direction: column;
        max-width: 400px;
        justify-self: center;
        margin: 0 auto;
    }

    .contact-form-input-wrapper{
        position: relative;
    }

    .contact-form-input-wrapper label{
        position: absolute;
        left: 0;
        top: 5px;
        color: #7f7f7f;
        font-family: NunitoRegular, sans-serif;
        transition: 0.2s top, 0.2s color;
    }

    .contact-form-input{
        height: 30px;
        min-width: 300px;
        border: none;
        border-bottom: 1px solid #7f7f7f;
        outline: none;
        margin-bottom: 30px;
        transition: 0.2s border-bottom-color;

        font-family: NunitoRegular, sans-serif;
        font-size: 14px;
    }

    .contact-form-input:focus {
        border-color: #313131;
    }

    .contact-form-input:focus ~ label, .contact-form-input:valid ~ label {
        top: -20px;
        color: #313131;
    }

    textarea.contact-form-input{
        resize: none;
        min-height: 100px;
    }

    textarea.contact-form-input ~ label {
        top: 0;
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