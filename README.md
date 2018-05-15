INTRODUCTION TO VIEW

#VUE SYNTAX
  <div id="app">
    {{ message }} <!-- referenced in data below-->
  </div>

  <script>
    var app = new Vue({
      el: '#app',
      data: {
        message: 'Hello Vue!'
      }
    })
  </script>

#Directives
Special attribute provided by Vue. Applies reactive behavior to the rendered DOM.
  * v-bind:title
    - keeps the element's title attribute up to date with the message property on the Vue instance
    - The title is what shows up on hover
        ex: <span v-bind:title="message"> <h2>Inventory</h2> </span>
  * v-if
    - Creates an if statement, if something is something do something
        ex: <span v-if="product.quantity === 0"> OUT OF STOCK </span>
  * v-for
    - Displays a list of items using the data from an Array
    - declares the singular version of variable name for the array
        ex:  <li v-for="product in arrayOfProducts"> {{ product.name }} </li>
  * v-on
    - attaches an event listener that invokes messages
        ex: <button v-on:click="product.quantity += 1"> Add </button>
        or this also works for click events
        ex: <button @click="product.quantity += 1"> Add </button>
  * v-model
    - binds form input and app state
    - I think this allows you to reference something into something like an input field
        ex: <input v-model="message">
  * v-model.number
    - says that this reference can only be a number
        ex: <input type="number" v-model.number="product.quantity">
