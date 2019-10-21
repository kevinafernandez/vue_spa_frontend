<template>
  <div>
    <b-row class="d-flex justify-content-center mb-3">
      <b-card
        title="Iniciar sesión"
        img-src="https://picsum.photos/600/300/?image=16"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          <b-form>
            <label class="sr-only" for="inline-form-input-name">Name</label>
            <b-input
              id="inline-form-input-name"
              class="mb-2 mr-sm-2 mb-sm-0"
              placeholder="Jane Doe"
            ></b-input>

            <label class="sr-only" for="inline-form-input-username">Username</label>
            <b-input-group prepend="@" class="mb-2 mr-sm-2 mb-sm-0">
              <b-input id="inline-form-input-username" placeholder="Username"></b-input>
            </b-input-group>

            <b-form-checkbox class="mb-2 mr-sm-2 mb-sm-0">Remember me</b-form-checkbox>

            <b-button variant="primary">Save</b-button>
          </b-form>
        </b-card-text>
      </b-card>
    </b-row>
  </div>
</template>
