<template>
    <div class="contact-form-input-wrapper"
         v-bind:class="{'has-value':hasValue}">
        <textarea v-if="textarea"
                  class="contact-form-input"
                  v-bind:class="className"
                  v-bind:name="name"
                  v-bind:id="id"
                  v-model="inputValue"
        ></textarea>

        <input v-else v-bind:type="type"
               class="contact-form-input"
               v-bind:class="{className}"
               v-bind:name="name" v-bind:id="id"
               v-model="inputValue"
        >

        <label v-bind:for="id">{{label}}</label>
    </div>
</template>

<script>
    export default {
        name: "FormInput",
        inheritAttrs: true,
        computed: {
            inputValue: {
                get() {
                    return this.value;
                },
                set(val) {
                    this.hasValue = (val !== '');
                    this.$emit('input', val);
                }
            }
        },
        props: {
            textarea: {
                type: Boolean,
                default: false
            },
            type: {
                default: 'text'
            },
            name: {
                type: String,
                default: ''
            },
            className: {
                default: ''
            },
            id: {
                type: String,
                default: ''
            },
            label: {
                default: 'Label'
            },
            onChange: Function
        },
        data: function () {
            return {
                value: '',
                hasValue: false
            };
        }
    }
</script>

<style scoped>
    .contact-form-input-wrapper{
        position: relative;
    }

    .contact-form-input-wrapper label{
        position: absolute;
        left: 1px;
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

    .contact-form-input {
        border-color: #313131;
    }

    textarea.contact-form-input{
        resize: none;
        min-height: 100px;
    }

    textarea.contact-form-input ~ label {
        top: 0;
    }

    .has-value label, .contact-form-input:focus ~ label {
        top: -20px !important;
        color: #313131;
    }




</style>