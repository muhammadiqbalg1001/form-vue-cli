<template>
    <form>
        <div class="row">
            <div class="col-xl-12">
                <h3>Contact Person</h3>

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
                    message: ''
                }
            }
        },
        methods: {
            submitForm() {
                console.log(this.formData);
            },
        }
    }
</script>