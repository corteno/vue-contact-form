<template>
    <div id="app">
        <ContactForm/>
    </div>
</template>

<script>
    import ContactForm from './components/ContactForm.vue'

    export default {
        name: 'app',
        components: {
            ContactForm
        }
    }
</script>

<style>
    #app {
      display: flex;
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    @font-face {
        font-family: NunitoRegular;
        src: url("./assets/fonts/Nunito-Regular.ttf");
    }

    @font-face {
      font-family: NunitoLight;
      src: url("./assets/fonts/Nunito-Light.ttf");
    }

    @font-face {
      font-family: NunitoBold;
      src: url("./assets/fonts/Nunito-Bold.ttf");
    }

</style>
