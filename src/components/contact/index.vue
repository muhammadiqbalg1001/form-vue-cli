<template>
    <form>
        <div class="row">
            <div class="col-xl-12">
                <h4>Contact Person</h4>

                <div class="form-group">
                    <label for="name">Nama</label>
                    <input 
                        type="text" 
                        id="name" 
                        class="form-control"
                        v-model="formData.name"
                    >
                </div>

                <div class="form-group">
                    <label for="email">Email</label>
                    <input 
                        type="email" 
                        id="email" 
                        class="form-control"
                        v-model="formData.email"
                    >
                </div>

                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input 
                        type="text" 
                        id="subject" 
                        class="form-control"
                        v-model="formData.subject"
                    >
                </div>

                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea 
                        type="text" 
                        id="message" 
                        class="form-control"
                        v-model="formData.message"
                    ></textarea>
                </div>

                <div class="form-group">
                    <p>Want to get promotion ?</p>
                    <div class="form-check">
                        <input 
                            type="checkbox" 
                            class="form-check-input"
                            value="Newsletter"
                            id="newsletter"
                            v-model="formData.extras"
                        >
                        <label 
                            for="newsletter" 
                            class="form-check-label"
                        >
                            Newsletter
                        </label>
                    </div>

                    <div class="form-check">
                        <input 
                            type="checkbox" 
                            class="form-check-input"
                            value="Promotions"
                            id="promotions"
                            v-model="formData.extras"
                        >
                        <label 
                            for="promotions" 
                            class="form-check-label"
                        >
                            Promotions
                        </label>
                    </div>
                </div>

                <div class="form-group">
                    <p>What are you ?</p>
                    <div class="form-check">
                        <input 
                            type="radio" 
                            class="form-check-input"
                            value="Male"
                            id="male"
                            v-model="formData.gender"
                        >
                        <label 
                            for="male" 
                            class="form-check-label"
                        >
                            Male
                        </label>
                    </div>

                    <div class="form-check">
                        <input 
                            type="radio" 
                            class="form-check-input"
                            value="Female"
                            id="female"
                            v-model="formData.gender"
                        >
                        <label 
                            for="female" 
                            class="form-check-label"
                        >
                            Female
                        </label>
                    </div>
                </div>

                <div class="form-group">
                    <label for="country">Country</label>
                    <select v-model="formData.country" class="form-control" name="option" id="option">
                        <option v-for="(country, index) in listCountry" :key="index">
                            {{ country }}
                        </option>
                    </select>
                </div>

                <button
                    class="btn btn-primary"
                    @click.prevent="submitForm"
                >
                    Submit
                </button>
            </div>
        </div>
    </form>
</template>

<script>
    export default {
        data() {
            return {
                formData: {
                    name: '',
                    email: '',
                    subject: '',
                    message: '',
                    extras: [],
                    gender: '',
                    country: ''
                },
                listCountry: [
                    'Indonesia',
                    'Malaysia',
                    'Singapore'
                ]
            }
        },
        methods: {
            submitForm() {
                console.log(this.formData);
            },
        }
    }
</script>