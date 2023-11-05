# cart

hosted-link=> https://tanishka-khamesara.github.io/cart/

Data Setup:

The code starts by defining an array named Products containing information about products, such as their id, name, and price.
Several variables are declared to store references to HTML elements in the document, such as productListView, shoppingCartListView, cartStatus, and totalPriceDisplay.
Another array called cart is initialized to store the products added to the shopping cart.
Rendering Product List:

The renderProductList function is responsible for rendering the list of products on the web page. It clears the existing product list, iterates through the Products array, and creates list items for each product.
For each product, it creates an HTML list item with the product name, price, and two buttons ("-" and "+") for adding and removing items from the cart.
These list items are added to the productListView element.
Rendering Shopping Cart:

The renderShoppingCart function updates the shopping cart view. It starts by clearing the existing shopping cart list and resetting the item counters (the spans with ids like count1, count2, and count3) to zero.
Then, it calculates the total price and iterates through the cart array, creating list items for each item in the cart.
The list items display the product name, price, quantity, and the total price for that item. It also includes a "-" button for removing items from the cart.
The function updates the cartStatus element to control its visibility. If the cart is empty, the "cartStatus" element is set to be displayed, indicating that the cart is empty. Otherwise, it's hidden.
Finally, it updates the totalPriceDisplay to show the total price of all items in the cart.
Adding Items to the Cart:

The addToCart function takes a productId as an argument and adds the corresponding product to the cart.
It first finds the product in the Products array based on the productId.
If the product exists, it checks if the product is already in the cart. If it is, it increases the quantity of that product in the cart. If not, it adds a new item to the cart with a quantity of 1.
After modifying the cart, it calls the renderShoppingCart function to update the cart view.
Removing Items from the Cart:

The removeFromCart function takes a productId as an argument and removes the corresponding product from the cart.
It finds the index of the product in the cart array based on the productId.
If the product is found and its quantity is greater than 1, it decreases the quantity by 1. If the quantity becomes 1, the product is removed from the cart.
After modifying the cart, it calls the renderShoppingCart function to update the cart view.
DOMContentLoaded Event Listener:

The code wraps the setup and rendering logic in an event listener for the "DOMContentLoaded" event. This ensures that the JavaScript code is executed only after the HTML document has been fully loaded.
It first calls renderProductList to display the initial list of products, and then it calls renderShoppingCart to display the initial shopping cart view.
Overall, this code provides a basic framework for an online shopping cart where users can add and remove products from their cart, and the cart's contents and total price are dynamically updated and displayed on the web page.
