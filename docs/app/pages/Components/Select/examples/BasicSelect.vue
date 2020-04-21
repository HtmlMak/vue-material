<template>
  <div>
    <div class="md-layout md-gutter">
      <div class="md-layout-item">
        <md-field>
          <label for="test">Test</label>
          <md-select v-model="test" name="test" id="test" multiple @input="test_method">
            <md-option v-for="option in data" :value="option" :key="option.id">{{option.name}}</md-option>
          </md-select>
        </md-field>
      </div>
    </div>

    <md-button class="md-primary md-raised" @click="movie = 'pulp-fiction'">Set Pulp Fiction</md-button>
  </div>
</template>

<script>
  export default {
    name: 'BasicSelect',
    data: () => ({
      movie: 'godfather',
      country: null,
      test: [
        {'id': 1, 'name': 'Club'},
        {'id': 2, 'name': 'Fight'},
      ],
      data: [
        {'id': 1, 'name': 'Club'},
        {'id': 2, 'name': 'Fight'},
      ],
      font: null
    }),
    methods: {
      test_method(val) {
        debugger
      },
    }
  }
</script>
