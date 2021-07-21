<template>
  <div>
    <ul class="grid grid-cols-3 gap-4 p-4">
      <li
        v-for="(item, index) in people"
        :key="index"
        class="border shadow p-4"
      >
        <img src="https://fakeimg.pl/250x250/cccccc" class="mx-auto mb-3">
        <h3 class="text-gray-700 font-semibold">
          {{ item.name }}
        </h3>
        <p>
          <slot name="hobby" :info="item.hobby" />
        </p>
        <p>
          <slot name="age" :info="item.age" />
        </p>
        <p>
          <slot name="job" :info="item.job" />
        </p>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      people: [
        {
          name: 'Joyce',
          hobby: 'shopping',
          age: '22',
          job: 'engineer'
        },
        {
          name: 'Alice',
          hobby: 'fishing',
          age: '30',
          job: 'hosekeeper'
        },
        {
          name: 'Catherine',
          hobby: 'browsing',
          age: '28',
          job: 'Police Officer'
        },
        {
          name: 'Oliver',
          hobby: 'jogging',
          age: '43',
          job: 'chef'
        },
        {
          name: 'Penny',
          hobby: 'diving',
          age: '18',
          job: 'student'
        }
      ]
    }
  }
}
</script>
