<template>
  <!-- 1. Template Syntax -->
  <div>
    <!-- a. Text Interpolation -->
    <p>{{ message }}</p>

    <!-- b. Raw HTML [v-html] -->
    <div v-html="rawHtml"></div>

    <!-- c. Attribute Bindings [v-bind:id] -->
    <button :id="buttonId">Click me</button>

    <!-- d. JavaScript expressions inside syntax i.e. {{ }} -->
    <p>{{ calculateSum(2, 3) }}</p>
  </div>

  <!-- 2. Methods -->
  <button @click="sayHello">Say Hello</button>

  <!-- 3. Reactivity Fundamentals [ref(), <script setup>] -->
  <p>{{ reactiveValue }}</p>

  <!-- 4. Computed Properties -->
  <p>{{ computedValue }}</p>

  <!-- 5. Class and Style Bindings -->
  <div :class="{ active: isActive }" :style="{ color: textColor }">Styled Div</div>

  <!-- 6. List Rendering -->
  <ul>
    <!-- a. v-for with an Object -->
    <li v-for="(value, key) in myObject" :key="key">{{ key }}: {{ value }}</li>

    <!-- b. v-for with a Range -->
    <li v-for="n in 5" :key="n">{{ n }}</li>

    <!-- c. v-for on <template> -->
    <template v-for="item in items" :key="item.id">
      <p>{{ item.name }}</p>
    </template>

    <!-- d. v-for with v-if -->
    <li v-for="item in itemsWithCondition" :key="item.id" v-if="item.active">{{ item.name }}</li>

    <!-- e. v-for with a Component -->
    <my-component v-for="item in items" :key="item.id" :item="item"></my-component>
  </ul>

  <!-- 7. Event Handling: Listening to Events [v-on:click] -->
  <button @click="handleClick">Click me</button>

  <!-- 8. Form Input Bindings -->
  <input type="text" v-model="textInput" />
  <input type="checkbox" v-model="isChecked" />
  <input type="radio" v-model="selectedRadio" :value="1" />
  <select v-model="selectedOption">
    <option value="option1">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
  <textarea v-model="textAreaInput"></textarea>

  <!-- 9. Watchers -->
  <p>{{ watchedValue }}</p>

  <!-- 10. Components -->
  <my-child-component :prop-value="parentValue" @custom-event="handleCustomEvent">
    <template #slotName>
      Content for slot
    </template>
  </my-child-component>

  <!-- 11. Router -->
  <!-- Assuming you have a router setup, use router-link or router-view here -->
</template>

<script>
import { ref, computed } from 'vue';

export default {
  data() {
    return {
      // 1. Template Syntax
      message: 'Hello, Vue!',
      rawHtml: '<span>Raw HTML</span>',
      buttonId: 'my-button',

      // 3. Reactivity Fundamentals [ref(), <script setup>]
      reactiveValue: ref('Reactive'),

      // 5. Class and Style Bindings
      isActive: true,
      textColor: 'blue',

      // 6. List Rendering
      myObject: { a: 1, b: 2 },
      items: [{ id: 1, name: 'Item 1' }, { id: 2, name: 'Item 2' }],
      itemsWithCondition: [{ id: 1, name: 'Active Item', active: true }, { id: 2, name: 'Inactive Item', active: false }],

      // 8. Form Input Bindings
      textInput: '',
      isChecked: false,
      selectedRadio: null,
      selectedOption: 'option1',
      textAreaInput: '',

      // 9. Watchers
      watchedValue: 'Initial Value',
    };
  },
  computed: {
    // 4. Computed Properties
    computedValue() {
      return this.message.toUpperCase();
    },
  },
  methods: {
    // 2. Methods
    sayHello() {
      alert('Hello!');
    },

    // 7. Event Handling: Listening to Events [v-on:click]
    handleClick() {
      console.log('Button clicked');
    },

    // 9. Watchers
    watchValue(newValue, oldValue) {
      console.log(`Value changed from ${oldValue} to ${newValue}`);
    },

    // 10. Components
    handleCustomEvent(payload) {
      console.log('Custom event received:', payload);
    },
  },
  watch: {
    watchedValue: 'watchValue', // 9. Watchers
  },
};
</script>

<style>
/* Styles for your component */
</style>
