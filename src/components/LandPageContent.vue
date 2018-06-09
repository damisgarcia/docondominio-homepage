<template>
  <div>
    <section id='sobre'>
    <div class="container">
      <div class="row">
        <div class="col">
          <h2 class="heading">Sobre</h2>
          <p>Reprehenderit dolore laboris incididunt occaecat consectetur tempor. Reprehenderit esse enim ipsum id enim nisi irure esse mollit fugiat ullamco culpa ex. Veniam quis laborum exercitation excepteur pariatur quis amet fugiat ullamco deserunt esse. Non nisi labore deserunt eiusmod veniam excepteur mollit occaecat commodo. Ullamco Lorem culpa sunt sint.</p>
          <div class="row">
            <div class="col-md-6 col-sm-12">
              <h4>Our Vision</h4>
              <p>Incididunt adipisicing exercitation deserunt aliquip proident et dolore. Eu sit incididunt nulla exercitation proident laborum esse.</p>
            </div>
            <div class="col-md-6 col-sm-12">
              <h4>Our Mission</h4>
              <p>Incididunt adipisicing exercitation deserunt aliquip proident et dolore.</p>
            </div>
          </div>
          <div class="row">
            <div class="col-md-6 col-sm-12">
              <h4>Awards</h4>
              <p>Incididunt adipisicing exercitation deserunt aliquip proident et dolore.</p>
            </div>
            <div class="col-md-6 col-sm-12">
              <h4>Perfection</h4>
              <p>Nulla reprehenderit minim excepteur qui et consequat qui.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    </section>    
    <section class="gray">
      <div class="container">
        <h2 class="heading">Fale conosco</h2>
        <div class="row">
          <div class="col">
            <b-form>
              <b-form-group id="exampleInputGroup1"
                            label-for="exampleInput1">
                <b-form-input id="exampleInput1"
                              type="email"
                              v-model="form.email"
                              required
                              placeholder="Enter email">
                </b-form-input>
              </b-form-group>
              <b-form-group id="exampleInputGroup2"
                            label-for="exampleInput2">
                <b-form-input id="exampleInput2"
                              type="text"
                              v-model="form.name"
                              required
                              placeholder="Enter name">
                </b-form-input>
              </b-form-group>
              <b-form-group id="exampleInputGroup3"
                            label-for="exampleInput3">
                <b-form-textarea id="exampleInput3"
                              type="text"
                              v-model="form.msg"
                              required
                              placeholder="Enter Message"
                              :rows="3"
                              :max-rows="6">
                </b-form-textarea>
              </b-form-group>
              <b-button type="submit" variant="primary">Submit</b-button>
              <b-button type="reset">Reset</b-button>
            </b-form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      form: {
        email: '',
        name: '',
        msg: null
      }
    }
  }
}
</script>
