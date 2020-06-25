<template>
    <div>
        <div class="container-fluid" style="padding:10%">
            <h2>Contact Me</h2>
            <form enctype="text/plain">
                <div class="form-group">
                    <input type="email" class="form-control"
                      v-model="contact.eamil" placeholder="Enter email">
                </div>
                <div class="form-group">
                    <textarea class="form-control"
                    v-model="contact.message" rows="3" placeholder="write message">
                    </textarea>
                </div>
            </form>
            <button type="button" @click="submit" class="btn btn-primary btn-lg">
                Contact
            </button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'contactModal',
  data () {
    return {
      contact: {
        email: '',
        message: '',
      }
    }
  },

  methods: {
    submit () {
      // validating the form
      if (this.contact.eamil !== '' && this.contact.message !== '') {
      // send details to email
        alert('Email sent!');
      } else {
        alert('All fields are required');
      }
    }
  }
}
</script>

<style lang="css" scoped>
  h2 {
    color: black;
  }
</style>
