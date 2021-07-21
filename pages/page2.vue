<template>
  <div>
    <h1 class="text-2xl">
      Page2
    </h1>
    <p>q = {{ $route.query.q }}</p>
    <hr>
    <h2 class="text-lg mb-4">
      Duplicate Components
    </h2>

    <ul class="flex flex-col space-x-0 md:flex-row md:space-x-3">
      <li v-for="index in 3" :key="index" class="mb-2">
        <Card
          :card-title="'Card' + index"
          :card-body="text"
          card-footer="here is footer"
        />
      </li>
    </ul>
    <hr>
    <h2 class="text-lg mb-4">
      Slot Component
    </h2>
    <form>
      <input id="hobby" v-model="checkedNames" type="checkbox" value="hobby">
      <label for="hobby">Hobby</label>
      <input id="age" v-model="checkedNames" type="checkbox" value="age">
      <label for="age">Age</label>
      <input id="job" v-model="checkedNames" type="checkbox" value="job">
      <label for="job">Job</label>
    </form>
    <List>
      <template v-for="item in checkedNames" #[item]="{info}">
        <!-- <p > -->
        {{ info }}
        <!-- </p> -->
      </template>
    </List>
  </div>
</template>
<script>
export default {
  data () {
    return {
      text:
        'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero ab totam explicabo libero doloremque quidem, numquam incidunt mollitia. Labore laborum magni, earum tempora rerum quae unde minima ea fuga quos itaque error illo delectus, perspiciatis, inventore excepturi illum. Fugiat, at.',
      checkedNames: []
      // options: ['hobby', 'age', 'job']
    }
  }
}
</script>
<style scoped>
hr {
  @apply my-4;
}
</style>
