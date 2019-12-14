<template>
  <div>
    <!--h1 v-once>{{ title }}</h1>
    <p>
      {{ getTitle() }}
    </p>
    <h1>{{ title }}</h1>

    <a v-bind:href="url">Google</a><br />
    <br />

    {{ link }}
    <p v-html="link"></p-->

    <!--counter /-->

    <!--counter /-->

    <!--kb-event /-->

    <!--twb /-->

    <!--div>
      <h1 v-if="show">Some title</h1>
      <h1 v-show="show">Some title</h1>

      <button @click="show=!show">Click Me</button>
    </div>

    <template v-if="true">
      <h1>Block 1</h1>

      <SimpleHeader v-if="wichOne == 1" title="Some other title" :color="color" />

      <SimpleHeader v-else-if="wichOne == 1 || wichOne == 2" title="Some other title 2" :color="color" />

      <SimpleHeader v-else title="Some other title 3" :color="color" />

    </template>

    <template v-else>
      <h1>Block 2</h1>

      <SimpleHeader v-if="wichOne == 1" title="Some other title" :color="color" />

      <SimpleHeader v-else-if="wichOne == 2" title="Some other title 2" :color="color" />

      <SimpleHeader v-else title="Some other title 3" :color="color" />

    </template-->

    <list :data='["Item 1", "Item 2", "Item 3"]' />

  </div>

</template>

<script>
import Counter from "@/components/Counter";
import KeyboardEvents from "@/components/KeyboardEvents";
import TwoWayBinding from "@/components/TwoWayBinding";
import SimpleHeader from "@/components/SimpleHeader";
import List from "@/components/List";

export default {
  name: 'app',
  components: {
    'counter': Counter,
    'kb-event': KeyboardEvents,
    'twb': TwoWayBinding,
    SimpleHeader,
    'list': List,
  },
  data() {
    return {
      title: "Some title",
      url: "https://google.com",
      link: "<a href=\"https://google.com\">Google</a>",

      color: "green",
      wichOne: 5,
      show: true,
    }
  },
  methods: {
    getTitle() {
      this.title = "Some other title";

      return this.title;
    },
    changeColor() {
      let r = Math.floor(Math.random() * 255).toString(16),
          g = Math.floor(Math.random() * 255).toString(16),
          b = Math.floor(Math.random() * 255).toString(16);

      this.color = `#${r}${g}${b}`;
    },
  },
}
</script>

<style>
#container {
  background-color: red;
}
</style>
