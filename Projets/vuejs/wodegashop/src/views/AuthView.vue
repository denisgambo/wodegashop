<template>
    <div class="container" v-if="sinUp">
  <div class="row justify-content-center">
    <div class="col-md-8 col-lg-6">
      <div class="card">
        <div class="card-header">
          Registration Form
        </div>
        <div class="card-body">
          <form>
            <div class="form-group row">
              <label for="nom" class="col-sm-3 col-form-label">Nom</label>
              <div class="col-sm-9">
                <input type="text" class="form-control" id="nom" placeholder="Votre nom">
              </div>
            </div>
            <div class="form-group row">
              <label for="prenom" class="col-sm-3 col-form-label">Prénom</label>
              <div class="col-sm-9">
                <input type="text" class="form-control" id="prenom" placeholder="Votre prénom">
              </div>
            </div>
            <div class="form-group row">
              <label for="telephone" class="col-sm-3 col-form-label">Téléphone</label>
              <div class="col-sm-9">
                <input type="tel" class="form-control" id="telephone" placeholder="Votre téléphone">
              </div>
            </div>
            <div class="form-group row">
              <label for="email" class="col-sm-3 col-form-label">Email</label>
              <div class="col-sm-9">
                <input type="email" class="form-control" id="email" placeholder="Votre email">
              </div>
            </div>
            <div class="form-group row">
              <label for="ville" class="col-sm-3 col-form-label">Ville</label>
              <div class="col-sm-9">
                <input type="text" class="form-control" id="ville" placeholder="Votre ville">
              </div>
            </div>
            <div class="form-group row">
              <label for="password" class="col-sm-3 col-form-label">Mot de passe</label>
              <div class="col-sm-9">
                <input type="password" class="form-control" id="password" placeholder="Votre mot de passe">
              </div>
            </div><br>
            <div class="form-group row">
              <div class="col-sm-9 offset-sm-3">
                <button class="btn btn-primary" type="submit">Envoyer</button>
              </div>
            </div>
          </form><br>
          <p>Already have an account? <a href="#" @click="showSinInForm"> Sin in herer</a></p>
        </div>
      </div>
    </div>
  </div>
</div>



<div class="container" v-if="sinIn">
  <div class="row justify-content-center">
    <div class="col-md-8 col-lg-6">
      <div class="card">
        <div class="card-header">Connexion</div>
        <div class="card-body">
          <form>
            <div class="form-group row">
              <label for="telephone" class="col-sm-4 col-form-label">Numéro de téléphone</label>
              <div class="col-sm-8">
                <input type="tel" class="form-control" id="telephone" placeholder="Votre numéro de téléphone">
              </div>
            </div>
            <div class="form-group row">
              <label for="password" class="col-sm-4 col-form-label">Mot de passe</label>
              <div class="col-sm-8">
                <input type="password" class="form-control" id="password" placeholder="Votre mot de passe">
              </div>
            </div><br>
            <div class="form-group row">
              <div class="col-sm-8 offset-sm-4">
                <button class="btn btn-primary" type="submit">Se connecter</button>
                
              </div>
            </div>
          </form><br>
          <p>You don't have an account? <a @click="showSinUpForm" href="#"> Register here</a></p>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
export default {
    data(){
        return {
            sinIn: true,
            sinUp: false,
        }
    },
    methods: {
        showSinUpForm(){
            this.sinUp = true
            this.sinIn = false
           
        },
        showSinInForm(){
            this.sinIn = true
            this.sinUp = false

        }
    }

}
</script>

<style>

</style>