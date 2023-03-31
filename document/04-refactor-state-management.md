# Session 4 - Refactor State Manage

In this session will do refactor state management.

### Problem

In the current code there is a little bug where when we navigate to `my orders` and go back to `get pizzas` we will lose the order pizza in the Index page. This is because it is stored in the list of pizzas in the current order on the Index component.

#### Before Refactoring 

Index page

There is one pizza on the order list on the right.
![](/images/session-4/refactor.jpg)

Navigating to `My Orders`
![](/images/session-4/refactor2.jpg)

Navigating back to `Get Pizza`
![](/images/session-4/refactor3.jpg)

As you can see the order pizza on the right is gone.

#### After Refactoring 

Index page

There is one pizza on the order list on the right.
![](/images/session-4/refactor4.jpg)

Navigating to `My Orders`
![](/images/session-4/refactor5.jpg)

Navigating back to `Get Pizza`
![](/images/session-4/refactor6.jpg)

And after reafactoring we can see that the order list on the right is saved after navigating back to index page from my orders.
