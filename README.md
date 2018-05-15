INTRODUCTION TO VIEW

V-FOR
- In my understanding this creates a variable that is a singular version in an array
    ex: v-for="product in arrayOfProducts">

V-IF
- Creates an if statement, if something is equal to something do something
    ex: <span v-if="product.quantity === 0">
          OUT OF STOCK
        </span>

@click
- Creates a click event, this example is used on a button
- Tell the click event what you want it to do
    ex: @click="product.quantity += 1"
